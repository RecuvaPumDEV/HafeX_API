## Get information about the bot

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