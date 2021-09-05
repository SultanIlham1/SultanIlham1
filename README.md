# ```Alphabot-Api```
<p align="center">
<a href="https://github.com/zeeoneofc/followers"><img title="Followers" src="https://img.shields.io/github/followers/zeeoneofc?color=red&style=flat-square"></a>
<a href="https://github.com/zeeoneofc/api-zeeoneofc/stargazers/"><img title="Stars" src="https://img.shields.io/github/stars/zeeoneofc/api-zeeoneofc?color=blue&style=flat-square"></a>
<a href="https://github.com/zeeoneofc/api-zeeoneofc/network/members"><img title="Forks" src="https://img.shields.io/github/forks/zeeoneofc/api-zeeoneofc?color=red&style=flat-square"></a>
<a href="https://github.com/zeeoneofc/api-zeeoneofc/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/zeeoneofc/api-zeeoneofc?label=Watchers&color=blue&style=flat-square"></a>
<a href="https://github.com/zeeoneofc/Rest-api-alphabot"><img title="Open Source" src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103"></a>
<a href="https://github.com/zeeoneofc/Rest-api-alphabot/"><img title="Size" src="https://img.shields.io/github/repo-size/zeeoneofc/Rest-api-alphabot?style=flat-square&color=green"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fzeeoneofc%2FRest-api-alphabot&count_bg=%2379C83D&title_bg=%23555555&icon=probot.svg&icon_color=%2300FF6D&title=hits&edge_flat=false"/></a>
<a href="https://github.com/zeeoneofc/Rest-api-alphabot/graphs/commit-activity"><img height="20" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"></a>&nbsp;&nbsp;
</p>
<p align='center'>
    </p>

-------
<h1 align="center">assalamu'alaikum <img src="https://user-images.githubusercontent.com/1303154/88677602-1635ba80-d120-11ea-84d8-d263ba5fc3c0.gif" width="40px" alt="hi"><br>I'm zeeone 😇 </h1>
<p align="center">
  <img src="https://c.top4top.io/p_2069qnvob1.jpg" />
</p>

- 👼 My name is Zeeone 
- 🗣️ I am 17 years old 
- 🔭 I am not programmer

## ```Connect with me```
<p align="center">
  <a href="https://instagram.com/zeeoneofc"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/> 
  <a href="https://wa.me/message/JBGU4J2DVYEDK1"><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <a href="https://www.facebook.com/profile.php?id=100015526687857"><img src="https://img.shields.io/badge/Facebook-%234267B2.svg?&style=for-the-badge&logo=facebook&logoColor=white" />
  <a href="https://t.me/zeeoneee"><img src="https://img.shields.io/badge/Telegram-%230088cc.svg?&style=for-the-badge&logo=telegram&logoColor=white" /> <br>
  <a href="https://github.com/zeeoneofc"><img src="https://img.shields.io/badge/-GitHub-black?style=flat-square&logo=github" /> 
  <a href="https://youtube.com/channel/UCdzWwbApjkyODby7_MoRYlA"><img src="https://img.shields.io/youtube/channel/subscribers/UCdzWwbApjkyODby7_MoRYlA?style=social" /> <br>
  <a href="https://komarev.com/ghpvc/?username=zeeoneofc&color=blue&style=flat-square&label=Profile+Dilihat"><img src="https://komarev.com/ghpvc/?username=zeeoneofc&color=blue&style=flat-square&label=Profile+Dilihat" />

</p>

## ```Api Features```
<details>
</Details>
1. 𝘿𝙤𝙬𝙣𝙡𝙤𝙖𝙙 & 𝙎𝙤𝙘𝙞𝙖𝙡 𝙈𝙚𝙙𝙞𝙖
<details>
<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'youtube_audio':  
      if (args.length < 1) return reply("Where's the link bro")
      if (!isUrl(args[0]) && !args[0].includes('youtu')) return reply('```Invalid link```')
      reply(lang.wait()) 
      anu = await fetchJson(`https://api-alphabot.herokuapp.com/api/yutub/audio?url=${args[0]}&apikey=Alphabot`)
      ini_txt = `YT AUDIO HAS BEEN FOUND\n\n`
      ini_txt += `• Judul : ${anu.result.title}\n`
      ini_txt += `• Ext : mp3\n`
      ini_txt += `• Size : ${anu.result.filesize}\n\n_Tunggu beberapa menit video akan segera di kirimkan_`
      ini_txt2 = await getBuffer(anu.result.thumb)
      ini_txt3 = await getBuffer(anu.result.result)
      alpha.sendMessage(from, ini_txt2, image, { quoted: mek, caption: ini_txt })
      alpha.sendMessage(from, ini_txt3, audio, { mimetype: 'audio/mp4', quoted: mek, ptt:true})
      break

```
</details>
2. 𝙄𝙨𝙡𝙖𝙢𝙞𝙘

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'hadist_sahih':
      if (args.length < 1) return reply(`Usage: ${prefix + command} kitab|nomor\nExample : ${prefix + command} Bukhari|15`)
      get_args = args.join(" ").split("|")
      kitab = get_args[0]
      nomor = get_args[1]
      var hadist = await fetchJson('https://api-alphabot.herokuapp.com/api/hadits?kitab=${kitab}&nomor=${nomor}&apikey=Alphabot')
      ini_result = hadist.result
      ini_txt = `Name : ${ini_result.name}\n`
      ini_txt += `Id : ${ini_result.id}\n`
      ini_txt += `Available : ${ini_result.availabel}\n`
      ini_txt += `Number : ${ini_result.contents.number}\n`
      ini_txt += `Arab : ${ini_result.contents.arab}\n`
      ini_txt += `Ind : ${ini_result.contents.id}`
      reply(ini_txt)
      break
```

</details>
3. 𝙄𝙢𝙖𝙜𝙚𝙨

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>


```
Example Case:

case 'wallpaper_programming':
     get_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/wallpaper/teknologi?apikey=Alphabot`)
     get_result = get_result.result
     for (var x = 0; x <= 5; x++) {
     var ini_buffer = await getBuffer(get_result[x])
     await alpha.sendMessage(from, ini_buffer, image)
     }
     break

```
</details>
4. 𝙍𝙖𝙣𝙙𝙤𝙢

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'random_quote':
     ini_result = await fetchJson('https://api-alphabot.herokuapp.com/api/randomquote?apikey=Alphabot')
     get_result = ini_result.result
     ini_txt = `${get_result.quotes}\n\n`
     ini_txt += `~ ${get_result.author}`
     reply(ini_txt)

```
</Details>
5. 𝙏𝙚𝙭𝙩 𝙈𝙖𝙠𝙚𝙧 2𝘿

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'maker_2d':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} zeeoneofc)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/maker?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
      ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>
6. 𝙏𝙚𝙭𝙩 𝙈𝙖𝙠𝙚𝙧 3𝘿

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'maker_3d':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} zeeoneofc)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/maker3d?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
      ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>
7. 𝙏𝙚𝙭𝙩 𝙈𝙖𝙠𝙚𝙧 𝙊𝙩𝙝𝙚𝙧𝙨

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'sertifikat_ff':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} zeeoneofc)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`api-alphabot.herokuapp.com/api/maker/special/epep?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
      ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>
8. 𝙋𝙝𝙤𝙩𝙤𝙤𝙭𝙮

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'coffe_cup':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} zeeoneofc)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://percobaannih.herokuapp.com/api/textmaker/senja?text=${teksnya}&theme=coffee-cup&apikey=Alphabot`}
      get_result = ini_result.result
      ini_img = await getBuffer(get_result.url)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>
9. 𝘼𝙣𝙞𝙢𝙚

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

case 'manga':
      if (args.length < 1) return reply(`Usage: ${prefix + command} naruto\nExample : ${prefix + command} naruto`)
      query = args.join(" ")
      var manga = await fetchJson('https://percobaannih.herokuapp.com/api/anime/kusonime?search=${query}&apikey=Alphabot')
      ini_result = manga.result
      ini_txt = `Title : ${ini_result.title}\n`
      ini_txt += `Title Japan : ${ini_result.title_jp}\n`
      ini_txt += `Genre : ${ini_result.genre}\n`
      ini_txt += `Season : ${ini_result.season}\n`
      ini_txt += `Producer : ${ini_result.producer}\n`
      ini_txt += `Type : ${ini_result.contents.number}\n`
      ini_txt += `Status : ${ini_result.availabel}\n`
      ini_txt += `Total Episode : ${ini_result.contents.number}\n`
      ini_txt += `Score : ${ini_result.contents.arab}\n`
      ini_txt += `Duration : ${ini_result.availabel}\n`
      ini_txt += `Release : ${ini_result.contents.number}\n`
      ini_txt += `Description : ${ini_result.contents.arab}`
      ini_txt2 = await getBuffer(ini_result.thumb)
      reply(ini_txt)
      break
```
</Details>
10. 𝘼𝙨𝙪𝙥𝙖𝙣 𝙏𝙞𝙢𝙚𝙡𝙞𝙣𝙚

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
11. 𝙉𝙎𝙁𝙒

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
12. 𝙂𝙖𝙢𝙚𝙨

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
13. 𝙂𝙖𝙘𝙝𝙖 𝘾𝙚𝙬𝙚

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
14. 𝙁𝙞𝙡𝙢𝘼𝙥𝙞𝙠

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
15. 𝙇𝙠21

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
16. 𝙉𝙚𝙬𝙨

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
17. 𝙀𝙣𝙘𝙤𝙙𝙚 & 𝘿𝙚𝙘𝙤𝙙𝙚

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
18. 𝙊𝙩𝙝𝙚𝙧𝙨

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
