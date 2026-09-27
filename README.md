# green-squares-bot

Fun + educational GitHub Actions bot that auto-commits on weekdays to keep your contribution graph active.

> Source in `green-squares-bot-main/` (`commit.py`, `.github/workflows/`).

## How it works
- Scheduled workflow (CRON) runs `commit.py`
- Appends to `daily_log.txt` / `commit_log.txt`, commits, pushes
- Tracking via `.commit_tracker.json`, `progress.md`

## Getting Started
1. Fork / clone this repo
2. Review `.github/workflows/` schedule
3. Enable Actions in your fork

Run locally:
```bash
cd green-squares-bot-main
python commit.py
```

## Tech
- Python, GitHub Actions, Git

## License
See inner `LICENSE`.
