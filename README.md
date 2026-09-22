Minecraft AI Chat Bot

A simple Minecraft AI chat bot built with Mineflayer
 and Ollama
.

Features

Per-user conversation memory

Automatic reconnect when disconnected

Username blacklist support

Automatic announcements explaining how to use the bot

Easy configuration

Customizable AI model

Mommy prompt support

Configurable chat cooldowns

Requirements

Node.js

Ollama

Qwen-Heretic or another compatible Ollama model

Mineflayer

Installation

Clone the repository:

git clone https://github.com/ExploitedTux/AiChatBot.git
cd AiChatBot


Install the required dependencies:

npm install


Pull your preferred Ollama model:

ollama pull qwen-heretic


Start the bot:

node AiChatBot.js

Configuration

Open AiChatBot.js and edit the configuration values at the top of the file.

You can configure:

Minecraft server address and port

Bot username

Server password

Ollama AI model

Username blacklist

Chat cooldowns

Other bot settings

The bot can use any Ollama model that is compatible with the configuration.

License

This project is licensed under the MIT License.
