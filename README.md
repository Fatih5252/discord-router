# discord bot router
oh hi, welcome to the discord router! if you are asking what a router is here is the answer:
<br>
a discord bot router is where you can create easely Slash commands!

### here is a tutorial:
- see the guide from [discord.js](https://discordjs.guide/)
- go to the Creating a bot section and then to the `creating Slash Commands` and in the Individual command files there you can see how to create an slash command
- if you cant find the section here is a link: https://discordjs.guide/creating-your-bot/slash-commands.html#individual-command-files 

### required things to do:
- go to src/functions/handelcommands and paste your client id in line 5
- go to your .env file and paste your bot token
- if you want guild commands then go to src/functions/handelcommands and paste your guild id in line 6 (if you want global commands then you can delete the line). !!WARNING!! but you must change some things, go to src/functions/handelcommands and line 28 - 32 and delete that line and paste this:

```js
await rest.put(
    Routes.applicationGuildCommands(clientId, guildId), {
        body: client.commandArray
    },
);
```

and yeah thats done :D Enjoy!
