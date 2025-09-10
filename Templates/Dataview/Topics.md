# Topics
```dataviewjs
(()=>{
const currentFile = app.workspace.getActiveFile();

if (!currentFile) {
    dv.paragraph("No active file");
    return;
}

const filename = currentFile.name;
const keyword = "Tutorials";

if (!filename.includes(keyword)) {
    dv.paragraph(`The filename must include "${keyword}" to get topic information.`);
    dv.paragraph(`Select the "${keyword} file and run this command to refresh:`);
    
dv.paragraph(`Dataview: Force refresh all views and blocks`);
    return;
}

// Extract the first part of file name up to and including the "-"
// For example, Extract "Git -" from "Git - Tutorials"
const index = filename.indexOf("-") + 1;
const parent = filename.substring(0, index)
const pages = dv.pages()
    .where(p => {
        return (
            p.file.name.startsWith(parent) && 
            p.Type === "Tutorial" &&
            p.Topics?.length > 0
        );
    });

const set = new Set();
pages.forEach(p => {
    p.Topics.forEach(t => set.add(t))
})

dv.list(Array.from(set).sort((a,b) => a.localeCompare(b)))
})()
```