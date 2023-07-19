## joinRole
Put this to GuildMemberAdd & guildMemberAdd event
```js
const hafex_api = require("hafex_api");
hafex_api.joinRole("GUILD_ID", "ROLE_ID", member)
```
### Example
```js
client.on(Events.GuildMemberAdd, (member) => {
    hafex_api.joinRole("1127649161219690646", "1130973660249862164", member)
});

client.on("guildMemberAdd", (member) => {
    hafex_api.joinRole("1127649161219690646", "1130973660249862164", member)
});
```