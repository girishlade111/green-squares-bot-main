# green-squares-bot

Fun + educational GitHub Actions bot that auto-commits on weekdays to keep your contribution graph green.

> Source lives in `green-squares-bot-main/` (`commit.py`, `.github/workflows/`).

## Features

- Scheduled CRON workflow runs `commit.py` automatically on weekdays
- Appends activity to `daily_log.txt` / `commit_log.txt` and pushes a commit
- Progress tracking via `.commit_tracker.json` and `progress.md`
- Zero setup beyond enabling GitHub Actions — fully self-contained

## Tech stack

- Python 3 (`commit.py`)
- GitHub Actions (scheduled workflows)
- Git

## How it works

1. A scheduled workflow (CRON) triggers `commit.py`
2. The script appends a line to the log files
3. Changes are committed and pushed automatically
4. Tracker files record per-run state and long-term progress

## Quick start

```bash
git clone https://github.com/girishlade111/green-squares-bot-main.git
cd green-squares-bot-main
```

Run locally:

```bash
cd green-squares-bot-main
python commit.py
```

To run it on a schedule:

1. Fork / clone this repo
2. Review and adjust the schedule in `.github/workflows/`
3. Enable GitHub Actions in your fork

## Project structure

```
green-squares-bot-main/
├── commit.py             # bot script: appends log entries
├── .github/workflows/   # scheduled CI workflows
├── commit_log.txt        # commit activity log
├── daily_log.txt         # daily activity log
├── progress.md           # progress notes
├── inspiration.txt       # project notes
└── LICENSE              # license
```

## Deploy notes

No deployment — this is a CI/CD automation bot. It runs inside GitHub Actions on a cron schedule.

---

Built by Girish Lade — https://ladestack.in
