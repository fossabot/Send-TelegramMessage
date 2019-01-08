# Send-TelegramMessage

A PowerShell Cmdlet to send messages using Telegram API

## Description
The Cmdlet is based on [mskellerman](https://github.com/mkellerman)'s [PSTelegramAPI](https://github.com/mkellerman/PSTelegramAPI). A config file (`config.xml`) is created for manageability causes.
A `dat` file is created after Telegram API verification. A log file is created on the first run.

## Requirements
* Telegram API is based on a phone number. So you will need a phone number dedicated to use for your notifications.
* You need a Telegram API ID for your client. To obtain the the id and hash you should follow [Telegram API docs](https://core.telegram.org/api/obtaining_api_id)
* [mskellerman](https://github.com/mkellerman)'s [PSTelegramAPI](https://github.com/mkellerman/PSTelegramAPI) is needed:
```
Install-Module PSTelegramAPI -Scope CurrentUser
```

## Usage
1. Download the files to any directory you like.
2. After you obtained the credentials from Telegram API, just copy and paste to the `config.xml` file.
3. Type the Telegram usernames of people you want to notify in `usernames` part of config.
4. You are good to go. Just type the command and parameters like the example below.

```
Send-TelegramMessage -Message "Hello World"
```

NOTE: On the first run Telegram API will send the number you have provided a verification code, via Telegram not SMS. You can do it on any desktop, web or mobile client. It does not have to be on the device you run the script on. 