> Kod Türü: Javascript
> Kod Adı: İstatistik Komutu
> Sürüm: d.js v13

```js
const { MessageEmbed, version } = require("discord.js");
const prettyMilliseconds = require("pretty-ms");

module.exports.run = async(client, message, args,  Embed) => {

const netkreatifcomtr = new MessageEmbed() 
.setColor("RANDOM")

.addField("Bot Bilgileri",`
**Sunucu Sayısı:** \`${client.guilds.cache.size}\`
**Kullanıcı Sayısı:** \`${client.guilds.cache.reduce((a,b)=> a + b.memberCount, 0)}\`
**RAM Kullanımı:** \`${(process.memoryUsage().heapUsed / 1024 / 1024).toFixed(2)} MB\`
**Gecikme Hızı:** \`${client.ws.ping}ms\`
`,true)

.addField("Kütüphane Bilgileri", `
**Discord.js:** \`v${version}\`
**Node.js:** \`${process.version}\`
`,true)
.setFooter("Netkreatif.com.tr")
message.channel.send({embeds: [netkreatifcomtr]})}

module.exports.help = {
    name:"istatistik"
}
```
