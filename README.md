# Go's CLI Task Manager - Taskwarrior compatible (WIP)

This project is forked from the Charm's [Creating a Task Manager](https://github.com/charmbracelet/taskcli) 
tutorial.  I use Taskwarrior very often for managing my tasks, but I've been looking 
for a Task Warrior compatible CLI app based neither in C/C++ nor Java.

Charm's original idea was to built a task management CLI using [Cobra][cobra], with Lip Gloss
styles *and* viewable using their kanban board.

## Roadmap

- [x] Test all current functionality.
- [ ] Document issues and needs for improvement.
- [ ] Propose enhacements.
- [ ] Review project's layout.
- [ ] Plan backend technology migration.

### Tests

#### Data Storage
- [x] Set up a SQLite database.
    - [x] open SQLite DB
    - [x] add task
    - [x] delete task
    - [x] edit task
    - [x] get tasks

#### Making a CLI with Cobra
- [x] add CLI
    - [x] add task
    - [x] delete task
    - [x] edit task
    - [x] get tasks

#### Add a little... *Je ne sais quoi*
- [x] print to table layout with [Lip Gloss][lipgloss]
- [x] print to Kanban layout with [Lip Gloss][lipgloss]

### Pending tasks

#### Data Storage
- [ ] Change backend to document/key-value.
    - [ ] open DB?
    - [ ] add task
    - [ ] delete task
    - [ ] edit task
    - [ ] get tasks

#### Making a CLI with Cobra
- [x] add CLI
    - [x] add task
    - [x] delete task
    - [x] edit task
    - [x] get tasks

#### Add a little... *Je ne sais quoi*
- [x] print to table layout with [Lip Gloss][lipgloss]
- [x] print to Kanban layout with [Lip Gloss][lipgloss]: current status is very incomplete.


## Project Layout

`db.go` - here we create our custom `task` struct and our data layer.

`main.go` - our main file handles our initial setup including opening a
database and setting the data path for our application.

`cmds.go` - this is where we do all of our Cobra commands and setup for our
CLI.

[lipgloss]: https://github.com/charmbracelet/lipgloss
[charm]: https://github.com/charmbracelet/charm
[cobra]: https://github.com/spf13/cobra
[kanban-video]: https://www.youtube.com/watch?v=ZA93qgdLUzM&list=PLLLtqOZfy0pcFoSIeGXO-SOaP9qLqd_H6
