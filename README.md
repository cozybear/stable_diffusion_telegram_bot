Simple Stable Diffusion Telegram Bot. Spawns a Text2Image process via a local Automatic1111 WebUI API endpoint. 

# How it works
The bot forwards Telegram user input as a text prompt to the local API backend. When an image is done generating it is send back to the user. The bot also features a simple payment system and SQL database (SQLite3) to document jobs and basic user information. In addition, a simple Redis Queue handler was added to process multiple requests from different users in sequential order.

# Quick start
1. Clone repository
   ```bash
   git clone https://github.com/ltillmann/stable-diffusion-telegram-bot
   ```

2. Install required dependencies.
   ```bash
   pip3 install requirements.txt
   ```
   
4. Run a local instance of Automatic1111's WebUI [stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) (adapt prompt parameters and port if desired). 
5. Start a Redis Server [Redis](https://github.com/redis/redis).
6. Init your Bot on Telegram using BotFather and fill in your credentials in config file.
7. Run ./telegrambot.py script.
8. Use Bot. Type /start to begin.