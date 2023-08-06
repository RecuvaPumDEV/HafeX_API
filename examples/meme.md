## Generates a random meme

```js
const hafex_api = require("hafex_api");
hafex_api.meme("title") //Sends the name of the meme
hafex_api.meme("url") //Sends meme url
hafex_api.meme("likes") //Sends meme likes
hafex_api.meme("comments") //Send comments on memes
```

## Example

```js
const { SlashCommandBuilder, EmbedBuilder } = require('discord.js');
const hafex_api = require("hafex_api");

module.exports = {
  name: 'meme',
  description: '',
  data: new SlashCommandBuilder()
    .setName('meme')
    .setDescription('Send you a random meme'),

  async execute(interaction) {
    await interaction.deferReply({ ephemeral: false });

    try {
      const title = await hafex_api.meme("title");
      const url = await hafex_api.meme("url");
      const likes = await hafex_api.meme("likes");
      const comments = await hafex_api.meme("comments");

      const embed = new EmbedBuilder()
        .setColor('#0095FF')
        .setTitle('Meme')
        .setThumbnail('https://hafex.xyz/hafex.png')
        .setDescription(title)
        .setImage(url)
        .setFooter({ text: `HafeX Bot | 👍 ${likes} 💬 ${comments}`, iconURL: 'https://hafex.xyz/hafex.png' });

      await interaction.editReply({ embeds: [embed] });
    } catch (error) {
      console.error('Error fetching meme:', error);
      await interaction.editReply('Oops! Something went wrong while fetching the meme.');
    }
  },
};

```