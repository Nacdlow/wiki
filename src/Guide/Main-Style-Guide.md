# Main Style Guide

The following is the main technologies which we are going to use.

- Language: [Go](https://golang.org)
- Database: [XORM](https://xorm.io)
- Version control: Git + GitLab
- Project management: GitLab Boards + Issues + Milestones


The WhatsApp group shall be the media for messaging. Email
may also be used, so email must be checked at least once
a day.  

The GitLab group shall contain all of the following:

- Code source
- Project documentation
- Issue and milestone tracking
- Continuous integration (auto-builds)
- Wiki (such as this one)
- Reports
- Software development process management (scrum/kanban/etc)

## Software Development Process

The project shall follow the Kanban methodology in the
software development process.  

Tasks, ideas, and bugs shall all be listed in the issue tracker,
and the issue board shall be used as a Kanban board.

The following labels shall be created:

- `Bug`: For bugs, and unexpected behaviour.
- `Feature`: For features.
- `Won't fix`: Things which will not be fixed or added.
- `Enhancement`: Enhancements to the project.

Other labels would be created for progress in the Kanban board:

- `Must have`: To-do, with Must priority.
- `Should have`: To-do with Should priority.
- `In Progress`: Work in progress.
- `Refinement & Testing`: Function in testing and refinement phase.

Complete issues are marked close.

## Decision Making

If a decision couldn't be reached by consensus, each
member shall have a turn to voice their opinion on the matter,
then a vote shall be held by show of hands.  

Votes can only be held in meetings which are pre-scheduled, and
members absent from the meeting aren't able to vote.  

The leader may have a second vote in the case of a tie.  

Changes to this style guide must be approved by a vote.  

## Meetings

Meetings shall be scheduled, at least once a week, to discuss the project,
follow up on design choices, brainstorm, etc.  

Meetings shall be scheduled in a way which fits the schedule of all the
members, but this shall not be used as an excuse to not hold a meeting.  

Meetings are recorded (consent must be taken each time), and must be released
in a way accessible by the members. Recordings are recorded and uploaded by the designated
recorder in the team, or by another team member if the designated recorder is not
available during that meeting.  

Every meeting must be announced in advanced by at least a day, a wiki page
can be created for that meeting, listing the points to cover, and what is
covered, and any major decision or votes which was taken.  


## Code Style Guide

Code commited to the Git repositories shall be properly formatted,
and shall pass tests in the next stages of development.  

The code shall be formatted according to the default specification
of the language. If such does not exist, we shall adopt a popular
code style guide for that language, and follow it strictly.  

Every code repository shall contain a `Makefile` which allows the
compilation of the program, and may include testing and formatting.  

Every code repository shall contain a `README` file which contains
the following sections:

- Description: A brief description of the code repository, with purpose
and goal.
- Clone and Install: Instructions of cloning the repository and installing
or executing the program.
- Usage: Documentation on the usage, configuration, command-line options or
environment variables used by the program.

A `CHANGELOG` file shall also be included, including all the tagged versions
of the projects, including the changes from the previous version.


### Go-specific Style Guide

All code shall be run through the following commands:

- `go fmt ./...`
- `go vet ./...`
- `go test ./...`

And any issues arise from these commands shall be fixed before
commited to the repository.  

Any public function or variable shall be documented. This is optional,
but recommended for private functions and variables.  

#### Go project structure

**Note: This is a new proposed section.**  

- `assets`: Any files used by external programs run by the program (i.e. configuration
  file for an external generator program).
- `cmd`: Contains all the command-line commands.
- `models`: Contains all struct models for database, data binding/validation forms, configuration files.
- `modules`: Contains sub-packages for different modules of the project, such as...
  - `settings`: Which contains program configuration.
  - `utils`: A "catch-all" module for everything and anything which doesn't fit anywhere else. :)
  - Other package modules can be created here as needed.
- `public`: Any files here will be public facing for web, this is useful for hosting web assets such as
	JavaScript files, CSS, images, and fonts.
  - `js`: For JavaScript files, external libraries must be versioned. The main JS file should be called `main.js`.
  - `css`: For CSS files, external libraries must be versioned. The main CSS file should be called `main.css`.
- `routes`: Where routes functions live, handling GET and POST requests, templates, validation, rendering pages, etc.
- `templates`: Where all the HTML template files are stored.
  - `base`: Where base templates live, such as `head` and `footer`.

## Liaison communications log

The project liaison shall keep a log of all the communications with
the professors and the project manager. preferably on the wiki.

## Code of Conduct

We shall follow [The Lunduke Code of Conduct](http://lunduke.com/coc.html), which
simply states:

> Be Excellent to Each Other.

And that's it! Simple enough, huh?

## Revisions to this document

Any changes to this document must be approved by a vote before being enforceable.
All changes to this document must be logged in the revision log.

## Revision log

- rev0 *(1st October 2019)*
  - Initial version
