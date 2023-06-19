# DESCRIPTION OF METHODOLOGY FOR THIS PROJECT

## TEMPLATE WORKFLOW

Product Manager:	Onwuta Ebube Gideon

Dev site:	learn\_git

Branch deployed on dev site:	develop

Live site:	https://github.com/Ebuube/learn\_git/tree/main

Branch deployed on live site:	main

When starting a dev ticket, branch from:	develop

When starting a hotfix ticket, branch from:	hotfix-\<ticket id\>-description

When updating your work, use:	git pull

When merging your work post review, use:	git push origin main


## TICKET PROGRESSION

* **NOT NOW**: Any project that has not been deemed relevant for this work effort (or sprint. This is also referred as `product backlog`. It should be prioritized to give hints to the team on what should be worked on in the next work sprint

* **READY FOR WORK**: Prioritized tickets for this work iteration. They might be the blockers for tickets in the backlog, or simply the next piece the team has chosen to work on.
	> **Note**: This can be sub-categorized as `Ready for Development`, `Ready for Code Review`, `Ready for Testing`, `Ready for Client Approval`, and `Ready for Deployment`.

* **IN PROGRESS**: A developer is currently working on this ticket, or a quality assurance review is being done.
	> **Note**: This can be sub-divided into `In Development`, and `In Testing`.

* **COMPLETED**: The work has been finished, or has been canceled. Perhaps, there were follow-up tickets, but only very rarely should a ticket be reopened after it has passed a code review, quality assurance review, and a client review.


## BASIC WORKFLOW

1. As you begin a ticket, update the status in the ticket tracker to say the ticket is `In Progress`. This will notify your team about what you are currently working on, and will give you the number for the branch you will create to work on your ticket.

2. From the branch develop, create a new branch whose name includes the `ticket ID` and a terse description of the work. If you are working on tickets that have sub-tasks, ensure the branch name uses the most relevant ticket number. For bigger feature, this ticket might be referred to in your ticketing system as a `Meta ticket` or `Epic ticket`. If you are working on only part of the larger feature, you should use the smallest relevant ticket number. Your ticket system might refer to this as a `user story`, an `issue`, or `bug ticket`.

3. Work on your ticket, ensuring you keep the ticket branch up to date with any changes that might have been incorporated into the branch `master` since you started your work. Begin each commit message with the ticket number enclosed in square brackets: `[#1234]`.

4. Run relevant tests for your code to ensure typos and basic errors are caught. This may include a spellcheck, and a language syntax check ([linting](https://en.wikipedia.org/wiki/Lint_(software))). If you are working in a test driven environment you will definitely have additional tests to run.

5. When you have completed your work (or think you have!), make a final commit with the keyword `Resolves` and then the ticket number: `Resolves #1234`.

6. Optionally, push your ticket branch to the code hosting repository. With the keyword in place in your commit message, this will move your ticket tracker forward to the next step.

7. In your ticket tracker add a comment to the ticket to include a note about the rationale for the approach you took and some kind of proof that the work was been completed. For example, a screenshot of how the ticket changes the display on your local development environment. This acts as a sanity check later if, suddenly, things stop working.

8. Ensure the ticket branch is **up-to-date** and then **merge** your work in the branch `develop`, and, assuming there are no merge conflicts, push the updated branch to the central repository.

9. Assuming there were no new problems introduced by the new work (regressions), the ticket can be closed.

10. Finally, delete your local ticket branch and the remote copy of the ticket branch.

> ### NOTE:
	* In some ticketing systems, adding a pound sign (#) will automati‐
	cally link the commit message to the ticket number. Adding square
	brackets around the ticket number will ensure that commit mes‐
	sages aren’t omitted if you choose to rebase your work because lines
	beginning with a # are ignored when commit messages are auto‐
	matically composed for the new commit objects. In many systems,
	including the keyword “resolves” will automatically move a ticket
	from In Progress to the next state (for example, Needs Testing or
	Closed); this will vary depending on the ticketing system you’re
	using. Check the documentation for whatever system you are
	using.


## ISSUE-BASED VERSION CONTROL

### The basic `ticket` for issues has three main parts:

* ***Card***:
	- A [terse](https://en.wiktionary.org/wiki/terse) description of the problem, written from the perspective of the user


* ***Conversation***:
	- Details about the problem you are trying to solve; where possible, it should avoid prescribing solutions

* ***Confirmation***:
	- The steps a user (from the first part) will be able to take to verify the problem has been solved


### For Milestones:


```
# Brief Summary:
A brief summary of what the issue will solve.

## Objective of task:
Explicit declaration of tasks to be completed for this milestone

# Relevant documentation:
Resources that will help those solve issues in this milestone

# Estimated length of task:
The time it could take to resolve this issue

# Timeline for task:
The date this task ought to be completed.

# Dependencies on other work:
How will this affect other works done or in progress (or future).

# Example of similar work:
A previous work done that solves a similar problem. Along with its `issue number` as a reference.

# Help:
Resources that might lend extra help to those who will engage in this milestone
```

### PROCESS OF DOING WORK

1. Create a new ticket in your issue tracking system; note the number on the issue.

2. In your local repository, create a new branch using the format `issuenumber-description`.

3. Do the work described in the ticket (and only the work described in the ticket).

4. Test your work and make sure it is complete and correct. Ensure it passes your QA test from the ticket you wrote in the development environment.

5. You now have a **dirty** working directory that contains new and/or modified files. Add your changes to the staging area of your local repository.

6. Commit your staged changes to the repository.

7. Push your changes to a backup server. In many cases, this will also be where your tickets are being tracked, such as Git-Lab, Bit-bucket, or `GitHub`. Depending on your ticketing system, the ticket may now be marked as `resolved` but not necessarily `closed`.

8. When you are completely satisfied with your work, `merge` your ticket branch into your main branch (usually `master`) and push the revised branches to the code hosting system.

9. Test your work again to ensure there are no follow-up issues.

10. Update your ticket as appropriate to close it out.
