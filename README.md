# HafeX_API

[WEBSITE](https://hafex.xyz/)
<img src="https://hafex.xyz/hafex_100.png" style="width:50px;height:50px;" align="right"/>
THIS IS ONLY FOR DISCORD.JS V14 & NODE.JS V18 OR HIGHER

HafeX_API is a Discord bot library that offers simple and useful features for developers. This API can assist Discord bot developers in the following ways:

Message Management: HafeX_API allows sending messages to text channels, editing messages, and deleting messages. This enables developers to create interactive and responsive bots that can communicate with users.

User Management: The API provides access to user information, such as their name, ID, avatar, and more. This can be useful for personalizing and customizing bot behavior based on specific users.

Server (Guild) Management: HafeX_API provides access to server information, including the name, ID, member count, and more. This allows developers to retrieve information about the servers where their bot is present and adapt accordingly.

Role and Permission Management: The API enables the creation, modification, and deletion of roles on a server. Developers can automate the process of assigning roles to users based on various criteria.

Event Tracking: HafeX_API allows tracking and reacting to various events, such as incoming messages, user presence changes, server updates, and more. This enables developers to create interactive and dynamic bots that respond to different situations.

In the future, HafeX_API plans to expand its features and provide additional useful tools for Discord bot developers. This includes support for channel management, richly formatted messages, voice channels, and more. By doing so, the API helps Discord bot developers create more interactive and feature-rich bots that can better communicate with users and enhance their experience on the Discord platform.

## Install Package
```
npm install hafex_api
```

## Update Package
```
npm update hafex_api
```

## Remove Package
```
npm remove hafex_api
```


## Usage
Put, for example, index.js in the base file or bot launcher

```js
const hafex_api = require("hafex_api");
hafex_api.setToken("YOUR BOT TOKEN");
```

### Get information about the bot

```js
const hafex_api = require("hafex_api");
hafex_api.info("Name of the guild: ");
```
<img src="https://i.imgur.com/4vp7HHn.png" style="width: 300px;height: 200px;">

### Easy embed

```js
const hafex_api = require("hafex_api");
const embed = hafex_api.easyEmbed({
  title: "Testings with HafeX API",
  description: "This is cool yeah",
  color: "#000000",
  author: "Working hihi",
  author_image: "https://hafex.xyz/hafex.png",
  thumbnail_image: "https://hafex.xyz/hafex.png",
  footer_text: "Footer text",
  footer_image: "https://hafex.xyz/hafex.png",
  image: "https://hafex.xyz/hafex.png",
  fields: [
    { name: "Field 1 [INLINE TRUE]", value: "Value 1", inline: true },
    { name: "Field 2 [INLINE TRUE]", value: "Value 2", inline: true },
    { name: "Field 3 [INLINE FALSE]", value: "Value 3", inline: false },
    { name: "Field 4 [INLINE FALSE]", value: "Value 4", inline: false },
   ]
});
message.reply({ embeds: [embed] });
```
<img src="https://media.discordapp.net/attachments/1130927370933641326/1130966978279002303/image.png?width=352&height=520" style="width: 200px;height: 400px;">

### Join role

```js
const hafex_api = require("hafex_api");
hafex_api.joinRole("GUILD_ID", "ROLE_ID");
```

## License

ISC

## Related

`hafex_api` owner [GitHub](https://github.com/RecuvaPumDEV) codes of the bots & npm
