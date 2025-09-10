<%*
const todo = new GIC.Todo(moment(tp.file.title, GIC.DATE_FORMATS.NOTE.DAY))
const builder = new GIC.NoteBuilder(tp);
tR += await builder.createAgendaNote(
	tp.file.title,
	GIC.TIME_PERIOD.DAILY
)

const breadcrumbs = builder.createAgendaNoteBreadcrumbs(GIC.TIME_PERIOD.DAILY);
const start = breadcrumbs.lastIndexOf("[[");
const week = breadcrumbs.substring(start);
const filePath = tp.file.path(true).replace(".md", "");
_%>

## Tasks

[[Main Dashboard]] · [[Task List]]

- [ ] Urgent
    - [ ] [[Task - Dog teeth cleaning]] (Delegate)
    - [ ] [[Task - Violet move out]]
    - [ ] [[Tasks/Backlog/Task - Obsidian - Ghost In The Code Plugin]]
- [ ] High
    - [ ] [[Task - Perform 20 pull-ups]] ^jwhoyp
    - [ ] [[Task - Read Bible]] ^c30kzc
    - [ ] [[Task - Run 6 minute mile]] ^tzgtf1
- [ ] Medium
    - [ ] [[Task - Learn how to create a server in C Sharp]]
    - [ ] [[Task - Recreate Color Cards Email Parser in C Sharp]]
    - [ ] [[Task - Build an APP with ASPNET Core and Angular from Scratch]]
    - [ ] [[Task - Budgeting app]]
- [ ] Low
    - [ ] [[Task - Visit Red Top Mountain State Park]]
    - [ ] [[Task - Build 8-Bit computer]]
    - [ ] [[Task - Learn 3 guitar songs]]
- [ ] None
    - [ ] [[Task - Build 5 sites that we like]]

### Delegate

<span class="placeholder">No tasks</span>

## Schedule
### Due

<%*
let noTasks = '<span class="placeholder">No tasks</span>';
let today = "";

today += todo.createBills();
today += todo.createWeeklyAgenda();
today += todo.createSpiritual(breadcrumbs).trim();

tR += today === "" ? noTasks : today;
%>

### Spillover

<span class="placeholder">No tasks</span>

### Morning

- [ ] Add weight to weight logs
- [ ] Put on warm morning clothes
- [ ] Update yesterday's note
- [ ] Setup tasks for today
- [ ] Morning work
- [ ] Hygiene routine
    - [ ] Brush teeth
    - [ ] Floss
    - [ ] Put on deodorant
- [ ] Exercise routine
    - [ ] Push-ups
    - [ ] Squats
    - [ ] [[<% filePath %>#^jwhoyp|Pull-ups]]
    - [ ] Hollow body holds
    - [ ] Handstand pushups
    - [ ] [[<% filePath %>#^tzgtf1|Running]] > [[Task - Run 6 Minute Mile - Training Routine 2]]
    - [ ] Ride bike
- [ ] [[<% filePath %>#^c30kzc|Bible]] > 1 day of plan
- [ ] Pray
- [ ] Preparation for the day
    - [ ] Pack food for work
    - [ ] Pack clothes for work
    - [ ] Dress for the bike ride

### Night

- [ ] Spend meaningful time with Kayla and Iljavik
- [ ] Plan for tomorrow
- [ ] Prep for tomorrow
    - [ ] Pick out clothes for tomorrow
        - [ ] Work clothes
        - [ ] Exercise clothes
    - [ ] Set things out for work
        - [ ] Work laptop
        - [ ] Car keys
        - [ ] Wallet
        - [ ] Wedding ring necklace
        - [ ] Headphones
    - [ ] Lint roll hat
- [ ] Brush baby's teeth
- [ ] Brush teeth
- [ ] Stretch

## Repeating

- [ ] Dog tasks
    - [ ] Change water
    - [ ] Put out food
- [ ] Chores
    - [ ] Pick up house
        - [ ] Bathroom
        - [ ] Bedroom
        - [ ] Kitchen
        - [ ] Living room
    - [ ] Dishes
        - [ ] Clean dishes
        - [ ] Put dishes away
    - [ ] Laundry
        - [ ] Clean laundry
        - [ ] Put laundry away
    - [ ] Vacuum
    - [ ] Throw out trash

- [ ] Write out who to respond to
- [ ] Respond to messages
    - [ ] Respond to Discord messages
    - [ ] Respond to Facebook Messenger messages
    - [ ] Respond to LinkedIn messages
    - [ ] Respond to phone messages
- [ ] People to reach out to
- [ ] Go through email
    - [ ] Go through Master email
    - [ ] Go through Personal email
    - [ ] Go through Developer email
    - [ ] Go through Shop email
    - [ ] Go through Social email
    - [ ] Go through Work email
