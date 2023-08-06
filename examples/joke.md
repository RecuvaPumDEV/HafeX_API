## Generates a random joke

```js
const hafex_api = require("hafex_api");
hafex_api.joke("title") //Sends the name of the joke
hafex_api.joke("url") //Sends joke url
```

## Example

```js
const { SlashCommandBuilder, EmbedBuilder } = require('discord.js');
const hafex_api = require("hafex_api");

module.exports = {
  name: 'joke',
  description: '',
  data: new SlashCommandBuilder()
    .setName('joke')
    .setDescription('Send you a random joke'),

  async execute(interaction) {
    await interaction.deferReply({ ephemeral: false });

    const embed = new EmbedBuilder()
      .setColor('#0095FF')
      .setTitle('Joke')
      .setDescription(hafex_api.joke("title"))
      .setImage(hafex_api.joke("url"))
      .setThumbnail('https://hafex.xyz/hafex.png')
      .setFooter({ text: 'HafeX Bot', iconURL: 'https://hafex.xyz/hafex.png' });

    await interaction.editReply({ embeds: [embed] });
  },
};
```