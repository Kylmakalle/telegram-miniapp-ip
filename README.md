# Telegram Mini App IP
Get IP address of a Telegram user with a Mini App

This simple GitHub-hosted webpage will try to get an IP v4 address of the user who opened your page and will send it to your bot using [Telegram.WebApp.sendData](https://core.telegram.org/bots/webapps#initializing-mini-apps)


## Usage
1. Send your user a message with a [KeyboardButton](https://core.telegram.org/bots/api#keyboardbutton) and set `web_app.url` to `https://akentev.com/telegram-miniapp-ip/`
    - **NB:** You can't use this method with [InlineKeyboardButton](https://core.telegram.org/bots/api#inlinekeyboardbutton). It will require a setup for your own server.

2. The user will tap the button, and Telegram will warn user about IP access.
 <img src="https://github.com/Kylmakalle/telegram-miniapp-ip/assets/24507532/23b729bb-d222-40f5-bfb7-83d1bca5de13" width="297.33">

3. After User confirmation, webapp will quickly "blink" on user screen without showing any content. Your bot will receive a [Message](https://core.telegram.org/bots/api#message) with `web_app_data.data` json-encoded string in format `{"web_app_ip":"<IP>"}`.
    - Example data: `{"web_app_data":{"data":"{\"web_app_ip\":\"185.134.24.94\"}\", "button_text": "Share IP"}`

https://github.com/Kylmakalle/telegram-miniapp-ip/assets/24507532/34937cba-70b4-4218-b2ee-5b498855183e


## Important notice
**Please use it for good reasons** and explain to the user why you need access to such data.

Possible use-cases:
- Automatically get correct user timezone
- Get evidence for VAT calculation
- Manage content depending on the user's "real location" (remember, IP can be changed with VPN)


## License
[MIT](LICENSE)
