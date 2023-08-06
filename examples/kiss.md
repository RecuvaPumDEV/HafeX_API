## Generates a random kiss gif

```js
const hafex_api = require("hafex_api");
hafex_api.kiss(); //Sends the url of the kiss gif
```

## Example

```js
const { SlashCommandBuilder, EmbedBuilder } = require('discord.js');
const hafex_api = require("hafex_api");

module.exports = {
  name: 'kiss',
  description: '',
  data: new SlashCommandBuilder()
    .setName('kiss')
    .setDescription('The user to kiss'),

  async execute(interaction) {
    await interaction.deferReply({ ephemeral: false });

    const embed = new EmbedBuilder()
      .setTitle('Kiss')
      .setColor("#0095FF")
      .setImage(`${hafex_api.kiss()}`)
      .setThumbnail("https://hafex.xyz/hafex.png")
      .setDescription(`${user} he/shewas kissed by ${interaction.user}!`)
      .setFooter({ text: 'HafeX Bot', iconURL: 'https://hafex.xyz/hafex.png' });

    await interaction.editReply({ embeds: [embed] });
  },
};
```