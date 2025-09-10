<%*
try {
    await tp.file.move(`/Tasks/Completed/2025/${tp.file.title}`)
}
catch(e) {
    console.log(e);
}
_%>