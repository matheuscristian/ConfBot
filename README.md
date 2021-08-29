![ConfBot Logo](./assets/images/ConfBotLogo.jpg)

# Info
ConfBot is a configurable bot for Discord in order to help people who don't know how to program create their bots easily just by changing a json configuration file.
You can se the video:

https://youtu.be/2fnrp29tbT0

# ConfBot requires
- [NodeJS V16.6.2](https://nodejs.org/en/)
- [Discord.js V13.1](https://discord.js.org/#/)
## Install dependencies
Go to the Node JS website and download the latest version, then download the bot, go to its folder in the terminal and type:

`npm install discord.js`.

You can download the bot by clicking here:
[Download here!!](https://github.com/M4THEWS2/ConfBot/archive/refs/heads/main.zip)
or install the latest version.

# Index
- [How to use](https://github.com/M4THEWS2/ConfBot#how-to-use)
    - [Get Started](https://github.com/M4THEWS2/ConfBot#get-started)
    - [Functions & Commands](https://github.com/M4THEWS2/ConfBot#functions--commands)
- [Functions](https://github.com/M4THEWS2/ConfBot#functions)
    - [Embed](https://github.com/M4THEWS2/ConfBot#embed)
    - [Reply](https://github.com/M4THEWS2/ConfBot#reply)
    - [Send](https://github.com/M4THEWS2/ConfBot#send)
    - [Ban](https://github.com/M4THEWS2/ConfBot#ban)
- [Variables](https://github.com/M4THEWS2/ConfBot#variables)
- [Activities](https://github.com/M4THEWS2/ConfBot#activities)

# How to use
## Get started
Go to the website: https://discord.com/developers/applications, login to your account, and create a bot. Configure it how you prefer.

![Dicord Developer Portal Image](./assets/images/Discord-Developer-Portal.png)

Press copy token, go to the configuration file: `config.json` and paste your token there.

```json
"token": "TOKEN HERE",
"prefix": "!"
```

Go to the `boot` folder and open `init.bat`.

![Init.bat image](./assets/images/init.bat.png)

If everything opens correctly you are ready to proceed.

Now, to put the bot on your server, copy your bot's ID, go to the website: https://discordapi.com/permissions.html, paste the ID, check the administrator permissions and click on the link.

![Permission calculator image](./assets/images/permission-calculator.png)

You can open the `init.bat` on the boot folder again.

## Functions & Commands
Commands are what people will type, eg `!help`. Now functions are what will happen after people send the command, example: After typing `!help`, the bot sends a message saying something.
An example configuration:
```json
"name": "help",
"functions": [
    {
        "name": "embed",
        "embedContent": {
            "author": "",
            "title": "ConfBot Ajuda",
            "description": ">>> Este é o ConfBot!!!\n Para ter mais detalhes sobre a configuração deste bot, acesse: https://github.com/M4THEWS2/ConfBot/",
            "color": "",
            "thumnail (URL)": "",
            "image (URL)": ""
        }
    }
]
```
In the example above, the bot sends an embed message in the chat after someone dictates the `!help` command (the prefix is ​​also set), the function that sends the embed has its name: `embed`.

# Functions
## Embed
Send a MessageEmbed.
    
    - options:
        embedContent: Contains embed data, they can be:
            - author
            - title
            - description
            - thumnail
            - image
            - color
    
        reply: decides whether the embed will be sent as a reply.
## Reply
Just reply a message

    - options:
        content: The content of the message.
## Send
Send a message in the channel

    - options:
        content: The content of the message.
## ban
Bans the first mention of the sent message.

    - options:
        content: The content of the message. If all goes well.
        banErrorMessage: If the command is not entered correctly it sends this message.
        reply: If the message will be replied.

# Variables
You can also put variables in the text, for example: `{user mention} don't do this again!!`, in this text, the program will replace the `{user_mention}` with the user mention. There are several mentions, they are:
    
    - User mention: {user_mention}
    - User id: {user_id}
    - User name: {user_name}
    - Command: {command}
    - Prefix: {prefix}

# Activities
You can enter what your bot is currently doing!! Or simply put custom messages below his name. To do this, go to the `activities.json` file, and simply add the messages you want. For example:
```json
[
   {
       "msg": "!help se estiver precisando de ajuda!!",
       "type": "WATCHING"
   } ,
   {
       "msg": "Este é o ConfBot!!",
       "type": "PLAYING"
   },
   {
       "msg": "Baixe o ConfBot em: https://github.com/M4THEWS2/ConfBot",
       "type": "WATCHING"
   }
]
```
There are several types of activities:

`"WATCHING", "PLAYING", "STREAMING", "LISTENING", "CUSTOM", "COMPETING"`