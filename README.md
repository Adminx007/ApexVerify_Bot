# ApexVerify Bot

Telegram OTP verification bot built with `python-telegram-bot` and `httpx`.

## Requirements

- Python 3.12
- Virtual environment recommended

## Setup

1. Create and activate a virtual environment:

```bash
cd /workspaces/ApexVerify_Bot
python3 -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the bot

```bash
source .venv/bin/activate
python avb.py
```

## Background run

If you want the bot to keep running while the terminal is open, use:

```bash
nohup .venv/bin/python avb.py > bot.log 2>&1 &
```

Then you can check the bot log with:

```bash
tail -n 50 bot.log
```

## Files to keep private

- `BOT_TOKEN` and `API_KEY` are stored inside `avb.py`. Do not publish this file publicly.
- Local data files like `*.json` and `bot.log` are ignored by `.gitignore`.

## Notes

- `requirements.txt` contains the pinned dependency versions.
- The bot uses a user keyboard menu and an inline admin panel.
- For 24/7 uptime, deploy on a server or cloud VM rather than the current interactive container.
