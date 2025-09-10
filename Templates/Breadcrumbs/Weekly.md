<%*
const { NoteFactory, NoteBuilderFactory } = await cJS();
const Note = NoteFactory.create();
const NoteBuilder = NoteBuilderFactory.create();
const builder = new NoteBuilder({
    moment,
    Note,
    templater: tp
});
tR += builder.createAgendaNoteBreadcrumbs(Note.FREQUENCY.WEEKLY);
%>