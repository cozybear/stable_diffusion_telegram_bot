Software-as-a-Service (SaaS) Stable Diffusion Telegram Bot. Creates a Text2Image process via the local Automatic1111 WebUI API endpoint. 

The bot forwards Telegram user text input as a prompt to the API backend. When an image is done generating it is send back to the user. The bot also features a simple payment system and SQL database (SQLite3) to document jobs and basic user information. In addition, I added a simple Redis Queue to process multiple requests in sequential order.

To work:

1. Install requirements.
2. Run a local instance of the WebUI (adapt prompt parameters and port if desired). 
3. Start a Redis Server.
4. Create a Bot on Telegram using BotFather and fill in your credentials in config.py
5. Run telegrambot.py entrypoint.
6. Use Bot. Type /start to begin.