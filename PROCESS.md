# Assignment Planner development process

**Model:** Extreme Programming (XP), adapted for an individual CS445 project.

**Repository:** https://github.com/jacobdweigel-bot/Assignment_Planner-CS445

**Task board:** https://github.com/users/jacobdweigel-bot/projects/1

## Working cycle

Choose a small task from the prioritized backlog, write or update its acceptance check, make the change, run the relevant tests, and try the result in the browser. Review priorities weekly and keep one task in progress at a time. An XP iteration is one week; there are no Scrum roles or required Scrum sprint artifacts.

The board uses Todo (the backlog), In Progress, and Done. P1 is the highest priority. Move a task to In Progress when work starts. Move it to Done only after its acceptance check passes, relevant automated tests pass, and any changes are recorded in Git. A working implementation alone does not finish a browser acceptance task.

## Initial prioritized backlog

1. **P1 - Verify saved coursework survives a server restart.** Add and edit coursework using an isolated database, restart the server, and confirm that course details, assignment notes, due dates, and completion are preserved.
2. **P2 - Check overdue and seven-day date boundaries.** Confirm yesterday is overdue, today is not overdue, today through six days ahead is upcoming, seven days ahead is excluded, and completed work never counts as overdue.
3. **P3 - Check keyboard navigation and dialog focus.** Add and edit coursework without a mouse; confirm labeled controls, visible focus, Escape behavior, and focus returning after dialogs close.
4. **P4 - Check the planner at phone and desktop widths.** Confirm assignment forms, course controls, and the workload panel are usable at about 390px and at desktop width without horizontal overflow.
5. **P5 - Check combined filters and completion totals.** Combine course, status, and search filters; complete and reopen an assignment; confirm global totals and course progress remain correct.

## XP practices and solo limitations

Use small changes, simple design, frequent integration, refactoring, and automated regression tests. For new logic defects, first reproduce the failure with a test when practical. Run `python -m unittest discover -s tests -v` and `node --test tests/model.test.mjs` before marking affected work complete.

Pair programming and collective ownership are unavailable in a one-person project. A separate self-review is a practical substitute for some review work, but does not provide an independent second developer. I am a student user of the planner; that helps with feedback but does not replace feedback from other students. Browser acceptance testing remains separate from the automated suites.
