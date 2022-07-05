> **Paylaşan:** Ranxe#2053<br>
> **Kod Türü:** Javascript<br>
> **Kod Adı:** Mesaj Silme Komutu<br>
> **Sürüm:** d.js v13<br>

```js
const Discord = require('discord.js');
exports.run = function (client, message, args) {
if (!message.member.hasPermission("MANAGE_MESSAGES")) return message.reply("❌ Yetersiz İzin Hatası. Bu Komut İçin Mesajları Yönet Yetkin Olması Gerekiyor");
if (!args[0]) return message.channel.send("Silinecek mesajın miktarını yaz!");
message.delete()
message.channel.bulkDelete(args[0]).then(() => {
message.channel.send(`✅ ${args[0]} tane mesaj silindi`)
})
}
 
exports.conf = {
enabled: true,
guildOnly: true,
aliases: ['clear'],
permLevel: 1
};
 
exports.help = {
name: 'temizle',
description: 'Redo',
usage: 'temizle '
};
```
