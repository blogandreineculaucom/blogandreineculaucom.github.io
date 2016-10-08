---
title: Vista - Blocked Startup Programs
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - windows vista
---
So.. you get that annoying pop-up in the taskbar every time you boot up your shinny Vista?

The glitch is to remove that programme from startup - use "msconfig" (search for it in the Start Menu Search).

Then seach for "task" in the Start Menu as well - and run "Task Scheduler".

You will then need to create a new task. On the right you have "Create basic task"... you will definitely find your way.

*   Give it a name
*   Trigger: When I log on
*   Action: Start a program (& select the program)
*   Finish: Open Open the Properties dialog for this task when I click on Finish

Check "Run with highest privileges" and then under Settings tab, "Run this task as soon as possible after a schedule start was missed".

Done!

And no, there is no other easier way.. yet!