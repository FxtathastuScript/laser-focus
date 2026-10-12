# Laser Focus

A personal productivity tracker built around the **Laser Focus Ritual** (Veducation Academy): plan the week once, plan every night, finish with focus, and see your progress in one place.

**Live site:** https://fxtathastuscript.github.io/laser-focus/

It is a single static page (`index.html`) with no server and no sign-up. Everything you enter is saved in your own browser.

---

## The ritual it follows

| When | Sheet | What you do |
|---|---|---|
| Every Sunday | **Task Sheet** | Pick the week's tasks, split them into Deep and Shallow work, star priorities, set an ETF |
| Every night | **Session Sheet** | Plan tomorrow and answer the 8 questions for each session |
| Any time | **Daily Success Tracker** | See completion, streaks, time accuracy and milestone progress |
| Every Sunday | **Weekly Review** | Review the week, carry over unfinished tasks, reflect and rate it |
| Any time | **Goal & milestones** | Define goals, add milestones, link tasks to them |

## Features

### Task Sheet (weekly)
- Two sections: **Deep work** and **Shallow work** (lighter tasks).
- Each task has a **★ priority**, an **ETF** (estimated time of finishing), an **ATF** (actual time of finishing), an optional day of the week, and an optional goal or milestone link.
- Per-section totals for ETF and ATF, and a week completion bar.
- Move between weeks with the arrows, or jump to this week and next week.

### Session Sheet (nightly)
Every session has eight required questions:

1. What is the task? Explain it. *(If it cannot be written clearly, it cannot be done clearly.)*
2. What is the challenge today?
3. How will you perform it?
4. How much time will it take to finish? *(This sets the ETF.)*
5. What exact outcome do you want at the end of the session?
6. How will you make it a trackable progress sheet?
7. Write everything that could go wrong.
8. Don't-do list: what will guarantee failure?

Unanswered questions are outlined in red, and each session shows how many questions are left. Items you add here also appear on that day in the Task Sheet. Ticking one off in either place updates both. You can also pull unscheduled tasks from the week's Task Sheet in one click.

### Focus timer
- Every unfinished task and session has a **▶ Start focus** button.
- A timer bar stays at the bottom of every page. It shows the task, the elapsed time, and how much of the ETF is left. The bar turns red once you go over the ETF.
- **Pause** and **Resume** at any time. **Stop & log** adds the focused time to the task's ATF. A task can be timed in several sittings, and each sitting adds to the total.
- Ticking a task done while its timer runs logs the time first. Runs under 30 seconds are not logged.
- The timer keeps running if you close or reload the page. The browser tab title shows the running time.

### Daily Success Tracker
- Today's session completion and this week's task completion.
- Milestone tasks finished, and a **perfect-day streak** (days where every planned session was done).
- **Time discipline:** deep and shallow hours this week, total ETF vs ATF, overall time drift, and the share of tasks finished within their ETF.
- A 7-day completion chart and a colour-coded month calendar. Click any day to see its sessions.
- Progress bars for every goal and milestone.

### Weekly Review
- Pick any week. It defaults to the current week.
- Shows completion, deep and shallow hours, time drift, perfect days, priority tasks done, and session plans fully answered.
- A day-by-day strip shows each day's completion.
- **Unfinished tasks:** carry one, or all, into next week's Task Sheet. The task is copied with its type, priority, goal and ETF, and this week's numbers stay as they were.
- Goal progress for that week.
- **Reflection:** five questions (what went well, what didn't and why, where the ETF missed most, what to change, top 3 priorities for next week) and a 1–10 rating. Answers save as you type. The ETF question shows the week's biggest overrun as a hint.

### Goals & milestones
- Add, rename and delete goals and milestones.
- A milestone's progress is the share of its linked tasks that are finished.

### Export a progress report
Click **Export report** to download a one-page summary as a **PNG** or an **A4 PDF**.
- Periods: this week, this month, last 30 days, or all time.
- Styles: dark, or a light print-friendly version.
- Includes headline stats, a daily or weekly completion chart, deep vs shallow work, ETF vs ATF accuracy, goal progress and a list of recently completed tasks.
- A **This week** report also includes your Weekly Review answers and rating. Longer periods show your weekly ratings and their average.

### Theme and phone layout
- The button next to Export switches the theme: **Auto** (follows your device), **Light** or **Dark**. Your choice is remembered.
- The layout adapts to phones. The menu scrolls sideways, task rows put Day, ETF and ATF on one line, and the timer bar fits the screen.

### Backup
**Export backup** saves all your data as a `.json` file. **Import backup** restores it, which is also how you move your data to another browser or device.

## Entering time
ETF and ATF accept any of these: `90`, `1h30m`, `1.5h`, `1:30`, `45m`.

## Your data and privacy
- All data is stored in your browser's `localStorage`. Nothing is sent to any server.
- Data is stored separately for each web address and each browser. A new address, browser or device starts empty, so use **Export backup** and **Import backup** to move it.
- Clearing site data in your browser deletes your entries, so export a backup now and then.

## Tech
- Plain HTML, CSS and JavaScript in one file. No build step.
- [html2canvas](https://html2canvas.hertzen.com/) and [jsPDF](https://github.com/parallax/jsPDF) (loaded from cdnjs) create the PNG and PDF reports.
- Fonts from Google Fonts: Bricolage Grotesque, Manrope and JetBrains Mono.

## Run it locally
Download `index.html` and open it in any modern browser. Report export needs an internet connection to load its two libraries.

## Deploy
The site is served with **GitHub Pages** from the `main` branch, root folder. Any change pushed to `index.html` goes live about a minute later.
