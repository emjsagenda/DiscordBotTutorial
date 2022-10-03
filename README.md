# How to make a Discord Server bot

**Hello!**

Ill Teach You How To Make Your Discord Bot, but before we start coding, we need to preparate the bot.

## Creating The Bot

1. Access The [Discord Developer Portal<svg class="icon outbound" xmlns="http://www.w3.org/2000/svg" ariaHidden="true" focusable="false" x="0px" y="0px" viewBox="0 0 100 100" width="15" height="15"><path fill="currentColor" d="M18.8,85.1h56l0,0c2.2,0,4-1.8,4-4v-32h-8v28h-48v-48h28v-8h-32l0,0c-2.2,0-4,1.8-4,4v56C14.8,83.3,16.6,85.1,18.8,85.1z"></path><polygon fill="currentColor" points="45.7,48.7 51.3,54.3 77.2,28.5 77.2,37.2 85.2,37.2 85.2,14.9 62.8,14.9 62.8,22.9 71.5,22.9"></polygon></svg>](https://discord.com/developers/applications). 
2. Click on "New Application" button.
3. Choose a name and click on "Create".

And You Should See A Page Like This.

<img src="https://discordjs.guide/assets/create-app.ed82aede.png"></img>
###### Credits: https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot

U Can Change Bot Avatar, Description, Name And Etc, and after that you gonna need to go to "Bot" tab in the left pane.

<img src="https://discordjs.guide/assets/create-bot.44c7ea49.png">

Click on "Add Bot" and after that click on "Yes Do It!", and now your bot is done.

___

## Bot Token

> ***CAUTION!***
>
>This Section Is Important And Critical, Pay Attention, And Dont Share Your Bot Token **ANYWHERE**

After Creating The Bot, You'll See This

<img src="https://discordjs.guide/assets/created-bot.286c1bcf.png">

In this section you can configure everything from your bot, if its public or private, token, name, avatar, etc. Your bot token will be revealed if u press "Reset Token" and Confirm it, Ill Ask you to paste it on a part of the code, and if you lost the bot token, just go back to the page and reset to reveal it again

___

## Adding Bot To Your Server

To Create A Invite Link, go back to My Apps. click on the bot you made and go to OAuth2 page, and on the side bar you'll find the OAuth2 URL generator. Select the `bot` and `application.commands` options. after that a list of permissions will appear, you can configure it freely for what yout bot needs.

Copy the link and put onto your browser, you should see smth like this:

<img src="https://discordjs.guide/assets/bot-auth-page.e624796f.png">

Choose the Server you want to add it and click on "Authorize", and the bot is in your server!

**First Part Done!**
____

## Bot Initial Files

You can many ways to save your token, like *JSON* or *dotenv*, but ill use the ***Convencional Way***, just pasting the token in the code (not safe), if you want to post the code in Github or smth like that, use dotenv/Json and .gitignore

Heres is the syntax for

**JSON:**

```json
{
	"token": "your-token-goes-here"
}
```

**dotenv:**

WARNING! import the dotenv package to it work: 

*shell*:
```shell
npm install dotenv
```

*.env* file:
```dotenv
A=123
B=456
DISCORD_TOKEN=your-token-goes-here
```

___

## Create Main Code

Make a file called `index.js` and paste the base code:


```
// Require the necessary discord.js classes
const { Client, GatewayIntentBits } = require('discord.js');
const { token } = require('./config.json');

// Create a new client instance
const client = new Client({ intents: [GatewayIntentBits.Guilds] });

// When the client is ready, run this code (only once)
client.once('ready', () => {
	console.log('Ready!');
});

// Login to Discord with your client's token
client.login(token);
```

and now go onto your shell and run the code `node index.js`, and your bot maybe is online!

Congratulations, you made a discord bot!

___

# Full Discord.js Guide 

All the codes and stuff are used from the [Discord.js Guide<svg class="icon outbound" xmlns="http://www.w3.org/2000/svg" ariaHidden="true" focusable="false" x="0px" y="0px" viewBox="0 0 100 100" width="15" height="15"><path fill="currentColor" d="M18.8,85.1h56l0,0c2.2,0,4-1.8,4-4v-32h-8v28h-48v-48h28v-8h-32l0,0c-2.2,0-4,1.8-4,4v56C14.8,83.3,16.6,85.1,18.8,85.1z"></path><polygon fill="currentColor" points="45.7,48.7 51.3,54.3 77.2,28.5 77.2,37.2 85.2,37.2 85.2,14.9 62.8,14.9 62.8,22.9 71.5,22.9"></polygon></svg>](https://discordjs.guide/#before-you-begin), if you want to make commands, go to the site, there it explains EVERYTHING about discord.js.

## Licence

MIT Copyright Licence [here](LICENSE)
