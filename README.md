Minecraft AI Chat Bot
<p align="center"> <strong>A simple AI-powered Minecraft chat bot using Mineflayer and Ollama.</strong> </p> <p align="center"> <a href="https://github.com/ExploitedTux/AiChatBot"> <img src="https://img.shields.io/github/stars/ExploitedTux/AiChatBot?style=for-the-badge&color=yellow" alt="Stars"> </a> <a href="https://github.com/ExploitedTux/AiChatBot"> <img src="https://img.shields.io/github/forks/ExploitedTux/AiChatBot?style=for-the-badge" alt="Forks"> </a> <a href="https://github.com/ExploitedTux/AiChatBot/blob/main/LICENSE"> <img src="https://img.shields.io/github/license/ExploitedTux/AiChatBot?style=for-the-badge" alt="License"> </a> </p> <p align="center"> <a href="#features">Features</a> • <a href="#installation">Installation</a> • <a href="#configuration">Configuration</a> • <a href="#usage">Usage</a> • <a href="#license">License</a> </p>
Features
Feature	Description
AI Chat	Talk to an AI directly through Minecraft chat
Per-User Memory	Each player has their own conversation history
Auto Reconnect	Automatically reconnects after disconnecting
Username Blacklist	Block specific players from using the bot
Announcements	Automatically tells players how to use the bot
Ollama Support	Use different Ollama models
Cooldowns	Prevent chat spam with configurable cooldowns
Custom Prompt	Fully customizable system prompt
Easy Configuration	Main settings are located in one place
<details> <summary><strong>Requirements</strong></summary> <br>

You will need:

Node.js

Ollama

An Ollama-compatible AI model

Mineflayer

Recommended model:

qwen-heretic

</details>
Installation
<details> <summary><strong>1. Clone the repository</strong></summary>
git clone https://github.com/ExploitedTux/AiChatBot.git
cd AiChatBot

</details> <details> <summary><strong>2. Install dependencies</strong></summary>
npm install

</details> <details> <summary><strong>3. Install an Ollama model</strong></summary>

For example:

ollama pull qwen-heretic


You can replace qwen-heretic with another compatible Ollama model.

</details> <details> <summary><strong>4. Start the bot</strong></summary>
node AiChatBot.js

</details>
Configuration

Most configuration options can be found at the top of AiChatBot.js.

<details> <summary><strong>Minecraft Settings</strong></summary> <br>

Configure the Minecraft connection:

SERVER_HOST = "localhost"
SERVER_PORT = 25565
BOT_USERNAME = "AiBot"
PASSWORD = ""


Change these values to match your Minecraft server.

</details> <details> <summary><strong>AI Settings</strong></summary> <br>

Choose which Ollama model the bot uses:

OLLAMA_MODEL = "qwen-heretic"


Any compatible Ollama model can be used.

</details> <details> <summary><strong>Blacklist</strong></summary> <br>

Add usernames that should not be able to interact with the bot:

BLACKLIST = [
    "ExamplePlayer",
    "AnotherPlayer"
]

</details> <details> <summary><strong>Cooldowns</strong></summary> <br>

Configure how frequently players can send messages to the bot.

This can be useful for preventing spam and excessive requests.

</details> <details> <summary><strong>System Prompt</strong></summary> <br>

The bot's personality and behavior can be customized through its system prompt.

You can modify the prompt to change how the AI responds to players.

</details>
Usage

Once the bot is connected, players can communicate with it through Minecraft chat.

The bot keeps separate conversation history for each player, allowing multiple players to have their own conversations.

The bot can also automatically announce how to interact with it.

Example
<Player> hello bot

<AI Bot> Hello! How can I help you?

<Player> what are you doing?

<AI Bot> Just hanging around the server and talking to everyone.

Project Structure
<details> <summary><strong>View project structure</strong></summary>
AiChatBot/
├── AiChatBot.js
├── package.json
├── package-lock.json
└── README.md

</details>
Customization

The bot is designed to be easy to modify.

You can change:

Minecraft server settings

Bot username

Authentication

AI model

System prompt

Blacklisted players

Cooldowns

Announcement behavior

AI personality

Most changes can be made without modifying the core bot logic.

Links

GitHub Repository

Mineflayer

Ollama

License

Released under the MIT License.

See LICENSE for more information.

<p align="center"> Made with Mineflayer and Ollama </p>
