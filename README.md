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
1. Download & Social Media
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
2. Islamic

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
3. Images

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>


```
Example Case:

case 'wallpaper_programming':
     get_result = await fetchJson(`https://percobaannih.herokuapp.com/api/wallpaper/teknologi?apikey=Alphabot`)
     get_result = get_result.result
     for (var x = 0; x <= 5; x++) {
     var ini_buffer = await getBuffer(get_result[x])
     await alpha.sendMessage(from, ini_buffer, image)
     }
     break

```
</details>
4. Random

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
5. Text Maker 2D

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
6. Text Maker 3D

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
7. Text Maker Others

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
8. Photooxy

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
9. Anime

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
10. Asupan Timeline

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
11. NSFW

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
12. Games

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
13. Gacha Cewe

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
14. FilmApik

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
15. Lk21

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
16. News

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
17. Encode & Decode

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
18. Others

<details>

<summary> <b>Example Case</b> &#10003</summary><br/>

```
Example Case:

Pp
```
</Details>
