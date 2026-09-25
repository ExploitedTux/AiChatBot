<div align="center">
AiChatBot

An AI-powered Minecraft chat bot built with Mineflayer and Ollama.

Chat with an AI directly from Minecraft, give it a custom personality, and let it remember conversations with individual players.

<br> <a href="https://github.com/ExploitedTux/AiChatBot"> <img src="https://img.shields.io/github/stars/ExploitedTux/AiChatBot?style=for-the-badge&color=yellow" alt="Stars"> </a> <a href="https://github.com/ExploitedTux/AiChatBot"> <img src="https://img.shields.io/github/forks/ExploitedTux/AiChatBot?style=for-the-badge" alt="Forks"> </a> <a href="https://github.com/ExploitedTux/AiChatBot/blob/main/LICENSE"> <img src="https://img.shields.io/github/license/ExploitedTux/AiChatBot?style=for-the-badge" alt="License"> </a>

<br><br>

<a href="#features">Features</a> •
<a href="#installation">Installation</a> •
<a href="#configuration">Configuration</a> •
<a href="#usage">Usage</a> •
<a href="#support">Support</a>

</div>
Features

AI Chat — Talk to the bot directly through Minecraft chat.

Per-Player Memory — Each player gets their own conversation history.

Ollama Support — Run local AI models through Ollama.

Custom Personality — Change the system prompt to make the bot behave however you want.

Automatic Reconnects — Reconnect automatically when the bot gets disconnected.

Player Blacklist — Prevent specific players from interacting with the bot.

Cooldowns — Control how often players can use the AI and how quickly the bot sends messages.

Long Responses — Automatically splits longer AI responses into multiple Minecraft messages.

Startup Messages — Send a random message when the bot joins the server.

Config File — Keep server, AI, cooldown, and bot settings in one place.

Command Protection — Prevent AI output from accidentally being sent as Minecraft commands.

Requirements

Before running the bot, make sure you have:

Node.js

Ollama

A compatible Ollama model

A Minecraft server that allows your bot to connect

Node.js packages listed in package.json

Recommended Model

The bot works with any Ollama-compatible model.

The current configuration uses:

qwen-heretic


You can change this to any model you have installed in Ollama.

Installation

Clone the repository:

git clone https://github.com/ExploitedTux/AiChatBot.git
cd AiChatBot


Install the dependencies:

npm install


Install and set up Ollama, then make sure the model you want to use is available locally.

Check your installed models with:

ollama list


Start Ollama if it isn't already running.

Then configure config.json and start the bot:

node ChatBot.js

Configuration

The bot uses config.json for its main settings.

Example:

{
  "username": "AiBot",
  "password": "CHANGE_ME",
  "Ip": "localhost",
  "blacklist": [
    "ExamplePlayer"
  ],
  "msglist": [
    "Chat with me using ?ai",
    "Ask me something with ?ai"
  ],
  "AI_MODEL": "qwen-heretic",
  "MAX_HISTORY": 8,
  "AI_COOLDOWN": 6000,
  "CHAT_COOLDOWN": 8000,
  "MC_CHAT_LIMIT": 150,
  "MAX_CONTINUATIONS": 2,
  "RECONNECT_DELAY": 5000,
  "AI_PREFIX": "?ai"
}

Minecraft
"username": "AiBot",
"password": "CHANGE_ME",
"Ip": "localhost"


username is the Minecraft username used by the bot.

password is optional and is used for servers that require /login.

Ip is the address of the Minecraft server.

Blacklist

Players listed under blacklist will be ignored by the AI.

"blacklist": [
  "PlayerOne",
  "PlayerTwo"
]

Startup Messages

msglist contains messages the bot can randomly send after joining.

"msglist": [
  "Chat with me using ?ai",
  "Ask me something with ?ai",
  "What's up?"
]

AI Model

Choose the Ollama model used by the bot:

"AI_MODEL": "qwen-heretic"


You can replace this with any compatible model installed on your system.

Cooldowns
"AI_COOLDOWN": 6000,
"CHAT_COOLDOWN": 8000


AI_COOLDOWN controls how often an individual player can request an AI response.

CHAT_COOLDOWN controls the delay between messages sent by the bot.

Values are in milliseconds.

Conversation History
"MAX_HISTORY": 8


Controls how much conversation history is kept for each player.

Higher values give the AI more context but use more tokens and memory.

Response Length
"MC_CHAT_LIMIT": 150,
"MAX_CONTINUATIONS": 2


MC_CHAT_LIMIT controls the maximum size of each Minecraft chat message.

MAX_CONTINUATIONS controls how many times the bot can continue an AI response when the model reaches its output limit.

AI Prefix
"AI_PREFIX": "?ai"


Players use the prefix to talk to the bot.

Example:

?ai hello

Customizing the AI

The bot's personality is controlled by the system prompt inside ChatBot.js.

You can change it to whatever you want.

For example:

const MommyPrompt = `You are a friendly Minecraft player who enjoys talking with people on the server.`;


You can use this to create different personalities, speaking styles, or behaviors without changing the rest of the bot.

Usage

Start the bot:

node ChatBot.js


Once it joins the server, players can talk to it using the configured prefix.

Example:

<Player> ?ai hello

<AiBot> Hey! What's up?

<Player> ?ai what are you doing?

<AiBot> Just hanging around and talking to people.


Each player has their own conversation history, so conversations don't get mixed together.

Project Structure
AiChatBot/
├── ChatBot.js
├── config.json
├── package.json
├── package-lock.json
└── README.md

Customization

The bot is built to be easy to change.

You can customize:

Minecraft server

Bot username

Login password

AI model

AI personality

Chat prefix

Player blacklist

Conversation history

AI cooldown

Chat cooldown

Startup messages

Response length

Reconnect timing

Most settings can be changed directly through config.json.

Links

GitHub

Mineflayer

Ollama

Support

Need help or want to get in touch?

LEC Public Discord: discord.gg/6b6tlec

Discord: injectexploit / exploitedtux

License

This project is released under the MIT License.

See LICENSE for more information.

<div align="center">
Made with Mineflayer + Ollama
</div>
