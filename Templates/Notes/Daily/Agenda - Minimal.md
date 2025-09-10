<%*
tR += await new GIC.NoteBuilder(tp).createAgendaNote(
  tp.file.title,
  GIC.TIME_PERIOD.DAILY
)
_%>

## Tasks

<%*
tR += todo.createBills();
tR += todo.createWeeklyAgenda();
-%>
- [ ] Update yesterday's note
