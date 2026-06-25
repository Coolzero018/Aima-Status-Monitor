# --- Description ---
AIMA Status Monitor is a simple automated utility and Telegram bot designed to monitor active visa processing applications, document validation updates, and appointment slots on the official Portuguese AIMA portal (portal-renovacoes.aima.gov.pt). The program checks the web portal for data updates, compares them with previous states, saves timestamps to a local history ledger, and instantly sends alert messages via a Telegram bot if any changes are detected.

--- Features ---
- Periodic scanning and parsing of current application metrics directly from target validation portals.
- Automated tracking of state differences against cached records to prevent duplicate alerts.
- A time-stamped history ledger file to log and track the timeline of portal status shifts.
- A multithreaded monitoring daemon that queries changes every 2 minutes without blocking or freezing Telegram user interactions.
- Simple interactive command controls (/start, /url setup, /check overrides, and /history export) directly inside Telegram chat.

--- Donations ---
If you’d like to see this project continue or develop into a more advanced version, you can make a donation here: https://ko-fi.com/coolzero55894. This would mean that I haven’t wasted all those hours of work and effort.

--- Installation and Setup ---
1. Install the dependencies:
pip install -r requirements.txt

2. Configure authentication (create a bot_data.py file in the main folder and add your token):
token = "YOUR_TELEGRAM_BOT_TOKEN_HERE"

3. Start the bot application:
python bot.py

4. Interact with the bot in Telegram:
Use the /url command to supply your portal tracking link, then send /monitor to spin up the background tracker.

--- Licence ---
MIT Licence (see the LICENSE file)
