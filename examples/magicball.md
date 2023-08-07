## Generates a random response magic ball

```js
const hafex_api = require("hafex_api");
hafex_api.magicball() //Sends a random response from the magic ball
```

## Example

```js
const { SlashCommandBuilder, EmbedBuilder } = require('discord.js');
const hafex_api = require('hafex_api');

module.exports = {
  name: '8ball',
  description: '[question]',
  data: new SlashCommandBuilder()
  .setName("8ball")
  .setDescription('Ask the magic 8-ball a question')
  .addStringOption(option =>
    option.setName('question')
      .setDescription('Ask a yes-or-no question')
      .setRequired(true)
  ),

  async execute(interaction) {
    await interaction.deferReply({ ephemeral: false });

    const question = interaction.options.getString('question');

    const embed = new EmbedBuilder()
      .setColor("#0095FF")
      .setTitle(`8-Ball`)
      .setDescription(`**Your question:** ${question}\n**Magic 8-Ball says:** ${hafex_api.magicball()}`)
      .setThumbnail("https://hafex.xyz/hafex.png")
      .setFooter({ text: 'HafeX Bot', iconURL: 'https://hafex.xyz/hafex.png' });

    await interaction.editReply({ embeds: [embed] });
  },
};

```