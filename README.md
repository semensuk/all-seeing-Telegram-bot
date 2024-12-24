# all-seeing Telegram bot

The all-seeing Telegram bot operates in business mode, making it a powerful tool for Telegram Premium users. It allows the retrieval of the content of messages that other users have edited or deleted in private chats with the bot's owner. The bot retrieves the original content from its database and notifies the owner. Additionally, it identifies new users who message the owner and sends their Telegram ID.

---

## 🌟 Features

- **Track Edited Messages**
- **Track Deleted Messages**
- **Detect New Users**
- **Multilingual Support**

---

## ⚙️ Setup Instructions

### 🛠️ Step 1: Create a Telegram Bot and Enable Business Mode

1. Open Telegram and start a chat with [@BotFather](https://t.me/botfather):

   - Send `/start` and `/newbot`.
     - Enter the bot's name.
     - Set a unique username.
   - Copy the token provided by @BotFather.

2. Enable business mode:

   - Send `/mybots` to @BotFather and select your bot.
   - Go to **Bot Settings** → **Business Mode** → **Turn on**.

3. Add the bot to Telegram Business:

   - Navigate to **Telegram Settings** → **Telegram Business** → **Chatbots**.
   - Enter the bot's username.

---

### 🔍 Step 2: Get Your Telegram User ID

1. Start a chat with [@pfauberg\_bot](https://t.me/pfauberg_bot).
2. Send `/start` to the bot.
3. The bot will respond with your Telegram user ID. Copy this ID.

---

### 🔧 Step 3: Configure the Bot

1. Rename the `config_example.ini` file to `config.ini` in the root directory.
2. Replace the placeholder values with your own:

```ini
token - Your Bot Token here

user_id - Your Telegram User ID here

name - Your timezone here

language - Your language here
```

#### Timezone Configuration

1. Find your timezone [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).
2. Use the format `Region/City` (e.g., `Europe/London`) in your `config.ini` file.

---

### 🚀 Step 4: Install and Run

1. Clone the repository to your local machine:

```bash
git clone https://github.com/Pfauberg/all-seeing-Telegram-bot
```

2. Navigate to the project directory:

```bash
cd all-seeing-Telegram-bot
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

4. Run the bot:

```bash
python main.py
```

---

## 🌐 Language Support

To add a new language:

1. Use an existing file in the `languages/` directory (e.g., `en.py` or `ru.py`) as a template or create your own file.
2. Update the `language` parameter in `config.ini` (e.g., \`language = "en").

---

## 📩 Examples of Bot Notifications

### New User Alert

```plaintext
👤 [JOHN]
ID: 123123123
```

### Edited Message Notification

```plaintext
✏️ [JOHN] 123123123
Message from 24/12/24 22:03

Changed from:
"QWERTY"

To:
"123456"
```

### Deleted Message Notification

```plaintext
🗑️ [JOHN] 123123123
Message from 24/12/24 22:03

Deleted:
"123456"
```

---
