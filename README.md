# Focusboard

Focusboard is a private, local-first productivity dashboard for planning tasks and completing timestamp-based focus sessions. It turns a simple to-do list into a calm daily workspace without accounts, tracking scripts, or a backend.

## Problem it solves

Many productivity tools add noise before they help users start. Focusboard keeps the core loop visible: choose a task, decide its priority and due date, work in a focus session, and review real progress from the current day.

## Key features

- Task creation, editing, completion, deletion, priorities, and optional due dates
- All, Active, Completed, and Overdue filters with title search
- Task statistics and completion progress
- Focus and short-break timer with start, pause, resume, reset, and configurable durations
- Timestamp-based elapsed-time calculation that survives refreshes without double-counting
- Daily focus goal, today's completed tasks, and current-day session history
- Defensive localStorage parsing, clear-data control, validation, and responsive accessible UI
- Works as a static site on GitHub Pages

## Technologies

Focusboard uses semantic HTML, modern CSS, and vanilla JavaScript. It has no build step, framework, API key, backend, analytics script, or external runtime dependency.

## Run locally

Open `index.html` directly in a browser, or serve the folder with any static server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**, choose the default branch and `/ (root)`.
4. Save and open the generated project URL.

All links and assets are relative, so the app works from a GitHub Pages project path.

## Privacy and tracking limitations

Tasks, preferences, and session history are stored only in this browser's localStorage. Nothing is sent to a server. Local browser data does not sync across devices and may be lost if browser storage is cleared.

Focusboard measures elapsed sessions while the app is open or can recover a saved in-progress timestamp after refresh. It does **not** measure total device screen time, other browser tabs, other applications, or background activity outside Focusboard.

## Screenshots

Add genuine screenshots here after deploying the app. Recommended captures:

1. Desktop dashboard with active tasks and the focus timer.
2. Mobile layout showing task filters and the daily goal.
3. Completed-task and session-history state.

Store images in a folder such as `docs/screenshots/` and embed them with Markdown:

```md
![Focusboard desktop dashboard](docs/screenshots/desktop-dashboard.png)
```

## Future improvements

- Optional recurring tasks and calendar export
- More detailed weekly summaries based only on saved sessions
- Import/export of local data for a user-controlled backup
- Installable PWA support with an offline app shell

## Lessons learned

Focusboard is intentionally local-first: the most reliable analytics are the ones the app can explain from saved events. Timestamp-based timer state is more resilient than decrementing a counter, and progressive disclosure keeps task planning useful on small screens.
