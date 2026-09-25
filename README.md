<div align="center">
AiChatBot
AI-powered Minecraft chat bot using Mineflayer and Ollama

Chat with a local AI directly through Minecraft chat.





Features •
Installation •
Configuration •
Usage •
Customization •
Support

</div>
Features
Feature	Description
AI Chat	Talk to an AI directly through Minecraft
Per-Player Memory	Keeps a separate conversation for each player
Ollama	Run AI models locally through Ollama
Custom Personality	Change the bot's personality and behavior
Auto Reconnect	Automatically reconnect after disconnecting
Blacklist	Block specific players from using the bot
Cooldowns	Prevent spam and excessive AI requests
Chat Queue	Controls outgoing messages to avoid flooding chat
Long Responses	Splits long AI responses into multiple messages
Startup Messages	Sends a random message when the bot joins
Configuration	Keep your settings in config.json
Pathfinder	Includes Mineflayer Pathfinder support
Requirements

You will need:

Node.js

npm

Ollama

An Ollama-compatible model

A Minecraft server

The bot currently uses:

Mineflayer

Mineflayer Pathfinder

minecraft-data

Ollama

Recommended model

The default configuration uses:

qwen-heretic


You can use any compatible model installed in Ollama.

Installation
1. Clone the repository
git clone https://github.com/ExploitedTux/AiChatBot.git
cd AiChatBot

2. Install dependencies
npm install

3. Install Ollama

Download and install Ollama from:

https://ollama.com/

Check that it is installed:

ollama --version

4. Install your AI model

For example:

ollama pull qwen-heretic


Check your installed models:

ollama list

5. Configure the bot

Create a config.json file in the project directory.

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
    "Ask me something with ?ai",
    "I'm online!"
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

6. Start the bot
node ChatBot.js

Configuration

All of the main settings are stored in config.json.

Minecraft
{
  "username": "AiBot",
  "password": "CHANGE_ME",
  "Ip": "localhost"
}

Setting	Description
username	Minecraft username for the bot
password	Server login password
Ip	Minecraft server address

If your server doesn't require a login password, leave it empty:

"password": ""

AI Model
"AI_MODEL": "qwen-heretic"


This is the Ollama model used for conversations.

You can change it to any model available on your machine.

For example:

"AI_MODEL": "llama3.1"

Blacklist

Add players that should not be able to use the bot:

"blacklist": [
  "PlayerOne",
  "PlayerTwo"
]


The bot will ignore AI requests from these players.

Startup Messages

The bot can send a random message after joining:

"msglist": [
  "Chat with me using ?ai",
  "Ask me something with ?ai",
  "I'm online!"
]


A different message can be selected each time the bot joins.

Conversation History
"MAX_HISTORY": 8


Controls how much conversation history is kept for each player.

Each player has their own separate conversation.

AI Cooldown
"AI_COOLDOWN": 6000


Controls how often the same player can request an AI response.

The value is in milliseconds.

6000 = 6 seconds

Chat Cooldown
"CHAT_COOLDOWN": 8000


Controls the delay between messages sent by the bot.

8000 = 8 seconds


This helps prevent the bot from flooding chat.

Minecraft Chat Limit
"MC_CHAT_LIMIT": 150


Controls the maximum length of each message sent by the bot.

Long AI responses are automatically split into multiple messages.

AI Continuations
"MAX_CONTINUATIONS": 2


Controls how many times the bot can ask Ollama to continue a response if the model stops because it reaches its output limit.

Reconnect Delay
"RECONNECT_DELAY": 5000


Controls how long the bot waits before reconnecting after a disconnect.

5000 = 5 seconds

AI Prefix
"AI_PREFIX": "?ai"


Players use this prefix to talk to the AI.

Example:

?ai hello


You can change it to whatever you want:

"AI_PREFIX": "!ai"

Usage

Start the bot with:

node ChatBot.js


Once connected, players can use the configured prefix.

Example:

<Player> ?ai hello

<AiBot> Hey, what's up?

<Player> ?ai what are you doing?

<AiBot> Just hanging around and talking to everyone.


The bot keeps separate conversations for each player.

For example:

PlayerA
└── Conversation A

PlayerB
└── Conversation B

PlayerC
└── Conversation C

Customization

The bot's personality is controlled by the system prompt in ChatBot.js.

Example:

const MommyPrompt = `
You are a friendly Minecraft player.
Keep conversations casual and natural.
Keep responses relatively short.
`.trim();


You can change the prompt to create whatever personality you want.

Some examples:

Friendly Minecraft assistant

Server guide

Funny character

Roleplay character

NPC-style assistant

Technical helper

Custom AI personality

Project Structure
AiChatBot/
├── ChatBot.js
├── config.json
├── package.json
├── package-lock.json
├── README.md
└── LICENSE

Security

Do not upload your real server password or other private credentials to GitHub.

Add your configuration file to .gitignore:

config.json
node_modules/


If you accidentally publish a password, change it immediately.

Troubleshooting
The bot won't connect

Check:

The server IP is correct

The server is online

The Minecraft version is supported

Another bot isn't already using the same username

Your authentication settings are correct

Ollama isn't responding

Check that Ollama is running:

ollama list


Make sure the model from AI_MODEL is installed:

ollama list


If it isn't installed:

ollama pull qwen-heretic

The bot keeps reconnecting

Check the console for the actual disconnect reason.

Common causes include:

Duplicate username

Incorrect server version

Server kicks

Authentication issues

Network problems

Incorrect configuration

Project Links

GitHub Repository

Mineflayer

Mineflayer Pathfinder

Ollama

Support

If you need help or want to report a problem:

Discord

LEC Public Discord:

discord.gg/6b6tlec

Developer:

injectexploit

exploitedtux

GitHub

Open an issue on the repository:

https://github.com/ExploitedTux/AiChatBot/issues

License

AiChatBot is released under the MIT License.

See LICENSE for more information.

<div align="center">

Made with Mineflayer and Ollama

⭐ Star the repository if you enjoy the project.

</div>
