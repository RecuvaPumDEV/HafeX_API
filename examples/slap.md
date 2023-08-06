## Generates a random slap gif

```js
const hafex_api = require("hafex_api");
hafex_api.slap(); //Sends the url of the slap gif
```

## Example

```js
const { SlashCommandBuilder, EmbedBuilder } = require('discord.js');
const hafex_api = require("hafex_api");

module.exports = {
  name: 'slap',
  description: '',
  data: new SlashCommandBuilder()
    .setName('slap')
    .setDescription('The user to slap'),

  async execute(interaction) {
    await interaction.deferReply({ ephemeral: false });

    const embed = new EmbedBuilder()
      .setTitle('Slap')
      .setColor("#0095FF")
      .setImage(`${hafex_api.slap()}`)
      .setThumbnail("https://hafex.xyz/hafex.png")
      .setDescription(`${user} was slapped by ${interaction.user}!`)
      .setFooter({ text: 'HafeX Bot', iconURL: 'https://hafex.xyz/hafex.png' });

    await interaction.editReply({ embeds: [embed] });
  },
};
```