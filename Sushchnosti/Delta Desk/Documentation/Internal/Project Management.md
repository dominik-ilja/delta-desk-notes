---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Project Management

This document is an overview to the processes and standards for project management at Delta Desk.

## Backlog and Sprints

A backlog is a list of all the current items relating to a client or client's project. Each week, a sprint is created. Items from the backlog are added to the sprint. This allows us to easily see all the current items we have while documenting what we've done throughout the week.

Clients want to be able to see what work has been done throughout the week. With sprints, we can easily give a report of the work we've done.

## Tasks

### Tags

Tags are used to give high-level information about the item. In ClickUp, at most two tags will be displayed.

We typically use tags to describe what kind of work will be needed on the task. For example, is this a backend, database, or frontend task? We don't uses tags like "bug" because the "Task Type" will cover situations like that.

- back-end
- cloud
- database
- data-conversion
- front-end
- important - Red
- infrastructure

Tag colors should be the same unless there's a special reason to change the color. We don't want to every tag to bring attention to itself. The default color will be black.

### Task Types

Todo - Add descriptions to each type

These are the different categorizations of tasks within our system:

- Bugs
- Documentation
- Task
    - Chores
    - Configuration
    - Enhancements
    - Features
    - Infrastructure
    - Performance
    - Security
    - Technical Debt
    - Upgrades
    - Testing
- Investigation
    - Research

## Statuses

Statuses represent different stages in our development workflow. Items should generally progress forward through these stages, though they may move backward when issues are discovered that require additional work.

### Categories & Definitions

#### Not Started

##### To Do (Default)

- Initial state when an item is created
- Basic information captured but work has not begun
- _Who can move:_ Project managers, team leads

##### Ready To Start

- All required information is documented (requirements, acceptance criteria, designs, dependencies)
- Item is prioritized and assigned to a developer
- No blockers preventing work from beginning
- _Who can move:_ Project managers after requirements review

#### Active

##### In Progress

- Developer is actively working on the item
- Code changes, testing, or other development work is underway
- _Who can move:_ Assigned developer when work begins

##### Developer Review

- Initial development work is complete
- Developer is conducting self-review or peer review of changes
- Code quality checks and basic testing performed
- _Who can move:_ Developer when ready for internal oversight

##### Internal Review

- Josh/Dominik reviewing the change for technical accuracy and business requirements
- May include code review, functionality testing, or requirement validation
- _Who can move:_ Josh/Dominik after completing review

#### Done

##### Ready For Deployment

- All reviews passed and change is approved for production
- Item is queued for the next deployment window
- _Who can move:_ Project manager after client approval

##### Discontinued

- Item will not be worked on or delivered due to scope changes, priority shifts, or other business decisions. The reasoning for this should be documented in a comment on the item and an appropriate state or tag should be added
- All work on the item has permanently ceased and no further development is planned
- _Who can set:_ Project managers or team leads with stakeholder approval (client approval required for items that reached Client Review)

#### Closed

##### Complete

- Item has been deployed to production successfully
- No further work required
- Item is considered fully done
- _Who can move:_ Project manager after successful deployment

### Workflows

#### Standard

1. To Do
2. Ready To Start
3. In Progress
4. Developer Review
5. Internal Review
6. Client Review
7. Ready For Development
8. Complete

#### Revisions

If issues are found during the "Developer Review" phase:

1. Developer Review
2. In Progress
3. Developer Review

If issues are found during the "Internal Review" phase:

1. Internal Review
2. In Progress
3. Developer Review
4. Internal Review

If Issues are found during the "Client Review" phase:

1. Client Review
2. In Progress
3. Developer Review
4. Internal Review
5. Client Review

### State

A state is a sub-categorization that gives context to what's happening with a status. For example, an item could have a status of "To Do" and a state of "Needs Information". We can look at this and conclude that more information needs to be provided to move the task out of "To Do".

This extra piece of data allows us to better understand the specifics of what's going on with an item. Another example would be an item whose status is "Internal Review" and a state of "To Review". This provides us the extra context to know that we have not yet finished doing the internal review.

States are used when additional context beyond the status is needed to understand an item's current situation. Not every item requires a state - they're most useful when there are blockers, dependencies, or specific conditions affecting progress.

### Additional Notes

- Items requiring revisions should move back to "In Progress" regardless of which review stage identified the issues
- If significant scope changes occur during any review, the item may need to return to "Ready To Start" for re-planning. It may also be decided that the item will no longer be worked on at all. In this case, it should be set to the "Discontinued" status.
- Emergency fixes may bypass certain review stages with project manager approval

## Archiving

ClickUp has the ability to archive different pieces of content:

- Folders
- Lists
- Spaces
- Tasks

Archiving will be done periodically to reduce the amount of visual clutter maintaining a clean workspace. A common use for archiving will be sprints. Once a sprint is complete, its relevancy fades away.

Next, we'll cover when different items will be archived.

### Tasks

Individual tasks are typically archived because the item has become irrelevant. Some common reasons are:

- No longer relevant
- Requirement changes that makes the item redundant
- Cancellation
- Out of scope

When an item is archived, we want to follow these steps:

1. Set status to "Complete"
2. Add a tag called "Ca

Will go through the following process:

- Status is set to "Closed"
- State is set to a relevant value such as "Cancelled", "Out of scope", etc. or simply "Archived"
- Task is moved to a list which contains the archived tasks. For example, "Closed - Not Implemented".

The current task name is "Closed - Not Implemented", but could change.