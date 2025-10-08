---
cssclasses:
  - full_width
---

```dataviewjs
(() => {
// Get tasks from the current file
const file = app.workspace.getActiveFile();
if (!file) return;

const hideCompletedSubtasks = (task) => {
    return {
        ...task,
        children: task.children
            .filter((subtask) => subtask.task && !subtask.fullyCompleted)
            .map(hideCompletedSubtasks)
    }
}

const tasks = dv.page(file.path).file.tasks.where(task => !task.fullyCompleted);
tasks.values = tasks.values.map(hideCompletedSubtasks)

// Define priority order (lower number = higher priority)
const priorityOrder = {
    "Urgent": 1,
    "High": 2,
    "Medium": 3,
    "Low": 4,
    "None": 5,
    "": 5  // Default for tasks without priority
};

// Function to extract priority from task text
function getPriority(task) {
    const priorityMatch = task.text.match(/\[Priority::\s*([^\]]+)\]/);
    return priorityMatch ? priorityMatch[1].trim() : "";
}

// Function to extract due date from task text
function getDueDate(task) {
    const dueDateMatch = task.text.match(/\[Due::\s*([^\]]+)\]/);
    if (dueDateMatch) {
        return dv.date(dueDateMatch[1].trim());
    }
    return null;
}

// Function to clean task text by removing dataview tags
function cleanTaskText(task) {
    return task.text
        .replace(/\[Priority::\s*[^\]]+\]/g, '')  // Remove priority tags
        .replace(/\[Due::\s*[^\]]+\]/g, '')       // Remove due date tags
        .replace(/\s+/g, ' ')                     // Replace multiple spaces with single space
        .trim();                                  // Remove leading/trailing whitespace
}

// Create a custom comparator function for sorting
function taskComparator(a, b) {
    const dateA = getDueDate(a);
    const dateB = getDueDate(b);
    const priorityA = getPriority(a);
    const priorityB = getPriority(b);
    
    // First sort by date
    if (dateA && dateB) {
        const dateComparison = dateA.ts - dateB.ts;
        if (dateComparison !== 0) return dateComparison;
    } else if (dateA && !dateB) {
        return -1; // Tasks with dates come first
    } else if (!dateA && dateB) {
        return 1; // Tasks with dates come first
    }
    
    // Then sort by priority
    const priorityOrderA = priorityOrder[priorityA] || priorityOrder[""];
    const priorityOrderB = priorityOrder[priorityB] || priorityOrder[""];
    
    return priorityOrderA - priorityOrderB;
}

// Sort tasks using Dataview's sort method with custom comparator
const sortedTasks = tasks.sort(t => t, "asc", taskComparator);

// Display the sorted tasks in a table format
const tableData = sortedTasks.map((task, index) => {
    return [
        index + 1,                           // Index (1-based)
        cleanTaskText(task),                 // Task text (cleaned)
        getPriority(task) || "None",         // Priority
        getDueDate(task) || ""               // Due Date
    ];
});

dv.table(["Index", "Task", "Priority", "Due Date"], tableData);
})()
```