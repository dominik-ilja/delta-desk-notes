```dataviewjs
(()=> {
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

const tasks = dv.page(file.path).file.tasks.where((task) => !task.fullyCompleted)

tasks.values = tasks.values.map(hideCompletedSubtasks)
dv.taskList(tasks)
})()
```
