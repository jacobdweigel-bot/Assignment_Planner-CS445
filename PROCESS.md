# Assignment Planner Process

I'm using Extreme Programming (XP) for Assignment Planner. The main features already work, so my next step is to check how they work together and fix any problems I find. XP fits this because I can work on one small task, test it, and then decide what needs attention next.

**Repository:** https://github.com/jacobdweigel-bot/Assignment_Planner-CS445

**Task board:** https://github.com/users/jacobdweigel-bot/projects/1

## How I'll work

I'll plan my work a week at a time and start with the highest-priority task. Before changing anything, I'll decide what needs to work for that task to be finished. Then I'll make the change, run the relevant tests, and try it in the browser. I'll review what's finished at the end of the week and choose what to work on next.

My board has Todo, In Progress, and Done columns. Todo is my backlog, with P1 as the highest priority. I'll keep one task in progress at a time and move it to Done after I've checked the result, passed the relevant tests, and committed any changes.

## Backlog

1. **P1 - Verify saved coursework survives a server restart.** Use a separate test database, add and edit coursework, and restart the server. Check that the details and completion status are still there.
2. **P2 - Check overdue and seven-day date boundaries.** Check assignments due yesterday, today, six days ahead, and seven days ahead. Completed assignments should never show as overdue.
3. **P3 - Check keyboard navigation and dialog focus.** Add and edit coursework without a mouse. Check that I can see which control is selected, close dialogs with Escape, and return to the right control afterward.
4. **P4 - Check the planner at phone and desktop widths.** Check the forms, course controls, and workload chart at desktop width and about 390 pixels wide. Nothing should require scrolling sideways.
5. **P5 - Check combined filters and completion totals.** Use course, status, and search filters together. Complete and reopen an assignment, then check the dashboard totals and course progress.

## Testing

I'll keep changes small and clean up code as I work. When I find a logic bug, I'll add a test that reproduces it when possible, then fix it and run the tests again.

The test commands are:

```powershell
python -m unittest discover -s tests -v
node --test tests/model.test.mjs
```

I'll also check the app in the browser, since passing tests won't tell me whether a form is easy to use or fits on a phone screen.
