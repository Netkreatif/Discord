> Kod Türü: Javascript<br>
> Kod Adı: Instagram Gönderi Takipçisi<br>
> Sürüm: d.js v13<br>
```
# Kod test edilmemiştir.
```
```js
const Discord = require('discord.js');
const client = new Discord.Client({ intents: Object.values(Discord.Intents.FLAGS).reduce((a, b) => a + b) });

client.on('ready', () => {
  const { Tracker } = require('gets-from-username');
  new Tracker(client, 'INSTAGRAM_KULLANICI_ADI');
});

client.on('newPost', username => {
  return message.channel.cache.get("KANAL_ID")(username+' yeni bir gönderi paylaştı!')
});

client.login('BOT_TOKEN');
```
