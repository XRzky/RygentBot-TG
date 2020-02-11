# Telegram Private Message Bot

Telegram Private Message Bot

**This project has entered the status of random update. If you have no opinion on using `.NET`, you can consider using [pmcenter] (https://github.com/Elepover/pmcenter) as the PM robot solution.**

## Installation

### Preparation
* Create a bot and get its token
* Install Python and pip, then use pip to install `python-telegram-bot`

### Configuration
Open `config.json` and configure
```json
{
    "Admin": 0,
    "//1": "Admin ID (A digital ID)",
    "Token": "",
    "//2": "Bot Token",
    "Lang": "en",
    "//3": "Language Pack Name (Be careful! It's 'en'!)"
}
```
If you didn't set admin's ID previously, the user who sends `/setadmin` to the bot first will become the admin. You can edit `config.json` to change admin later.

## Upgrade
Replace `main.py` and folder `lang`, then run `main.py`

## Run
```
python main.py
```

## Usage

### Reply
Reply directly to the message forwarded by the robot to reply. You can reply text, sticker, photo, file, audio, voice and video.

### Inquire sender identity
You can reply `/info` to the message which you want to get its sender's info more clearly.

### Message sending notification
Send the command `/togglenotification` to the bot to enable/disable the message sending notification

Effect:
* For admin: After replying to the user, if there is no error, it will not prompt "replied"
* For users: After sending a message, the bot will not reply "received"

### Ban and unban
Reply `/ban` to a message to block the sender of the message from sending messages to you

Reply `unban` to a message or send `/unban <User ID>` to unban a user

## Available commands
| Command                | Usage                                      |
| :---                   | :---                                       |
| /ping                  | Check if the bot is running                |
| /setadmin              | Set the current user as admin              |
| /togglenotification    | Toggle message sending notification status |
| /info                  | Inquire sender identity                    |
| /ban                   | Ban a user                                 |
| /unban <ID (optional)> | Unban a user                               |
