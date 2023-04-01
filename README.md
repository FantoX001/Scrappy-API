<h1 align="center">Scrappy API</a>
</h1>

<h4 align="center">A 4 in 1 scraper API with `Genius Lyrics`, `Instagram`, `Facebook` and `Xvideos` scrapper.
</h4>

<p align="center">
<a href="#"><img title="Rest-Api" src="https://img.shields.io/badge/Free Rest Api-green?colorA=%23ff0000&colorB=%23017e40&style=for-the-badge"></a>
</p>

<p align="center">
<a href="https://github.com/FantoX001/Scrappy-AP/fork">
    <img src="https://img.shields.io/github/forks/FantoX001/Scrappy-AP?label=Fork&style=social">
    </a>
    
  <a href="https://github.com/FantoX001/Scrappy-AP/stargazers">
    <img src="https://img.shields.io/github/stars/FantoX001/Scrappy-AP?style=social">
  </a>

</p>

<p align="center">
<a href="https://github.com/inirey/Followers"><img title="Followers" src="https://img.shields.io/github/followers/FantoX001?color=blue&style=flat-square"></a>
<a href="https://github.com/FantoX001/Scrappy-API"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FFantoX001%2FScrappy-API&count_bg=%23FFA305&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Total+Hits&edge_flat=false)](https://hits.seeyoufarm.com"/></a>
</p>
  
</p>

<br>

## 🧩 Install dependencies:

```
npm i axios
```
<p align="center">
Or
</p>

```
yarn add axios
```

<br>

## 🧩 API Endpoints & Usage:


<br>

<h2 align="center">📥 Facebook video scraper:
</h2>


- Normal use:
```
const axios = require("axios");

async function main() {
    const queryURL = "PUT A PUBLIC FACEBOOK URL HERE ";
    
    let res = await axios.get("https://fantox001-scrappy-api.vercel.app/fbdl?url=" + queryURL)
    
    const scrappedURL = res.data.videoUrl
    
    console.log(scrappedURL)
  }
  
  main();
  
```

<br>

- In WhatsApp bot or any other bots:
```
// Note: Bot's code definition will vary from one bot to another. So please use it according to your bot's code.

const axios = require("axios");
const queryURL = args[0];

if(!args[0]){
  return reply('Please provide a public FB Vido URL to download video!');
}

let res = await axios.get("https://fantox001-scrappy-api.vercel.app/fbdl?url=" + queryURL)

const scrappedURL = res.data.videoUrl

// Send video through scrapped link
await client.sendMessage( m.chat,{ video: { url: scrappedURL }, caption: `_Scrappy API by: FantoX001_` },{ quoted: m });
  
```

<br> <br>

<h2 align="center">🎬 Instagram video scraper:
</h2>

- Normal use:
```
const axios = require("axios");

async function main() {
    const queryURL = "PUT A PUBLIC INSTAGRAM VIDEO OR REEL URL HERE";
    
    let res = await axios.get("https://fantox001-scrappy-api.vercel.app/instadl?url=" + queryURL)
    
    const scrappedURL = res.data.videoUrl
    
    console.log(scrappedURL)
  }
  
  main();
  
```

<br>

- In WhatsApp bot or any other bots:
```
// Note: Bot's code definition will vary from one bot to another. So please use it according to your bot's code.

const axios = require("axios");
const queryURL = args[0];

if(!args[0]){
  return reply('Please provide a public Instagram Video / Reel URL to download video!');
}

let res = await axios.get("https://fantox001-scrappy-api.vercel.app/instadl?url=" + queryURL)

const scrappedURL = res.data.videoUrl

// Send video through scrapped link
await client.sendMessage( m.chat,{ video: { url: scrappedURL }, caption: `_Scrappy API by: FantoX001_` },{ quoted: m });
  
```

<br><br>

<h2 align="center">🎼 Genius Lyrics scraper:
</h2>


- Normal use:
```
const axios = require("axios");

async function main() {
    const searchQuery = "heat waves"; // Put any precise and short song name instead of heat waves (Don't put - here).
    
    let res = await axios.get("https://fantox001-scrappy-api.vercel.app/lyrics?search=" + searchQuery)

    const thumbnail = res.data.thumbnail
    const lyrics = res.data.lyrics

    console.log(thumbnail)
    console.log(lyrics)
  }
  
  main();
  
```

<br>

- In WhatsApp bot or any other bots:
```
// Note: Bot's code definition will vary from one bot to another. So please use it according to your bot's code.

const axios = require("axios");
const searchQuery = args.join(" ");

if(!searchQuery){
  return reply('Please provide a song name to get lyrics.');
}

let res = await axios.get("https://fantox001-scrappy-api.vercel.app/lyrics?search=" + searchQuery)

const thumbnail = res.data.thumbnail
const lyrics = res.data.lyrics

// Send Album thumbnail and lyrics using scrapped data.
await client.sendMessage( m.chat,{ image: { url: scrappedURL }, caption: lyrics },{ quoted: m });
  
```
<br><br>

<h2 align="center">❌videos scraper:
</h2>

- Normal use:
```
const axios = require("axios");

async function main() {
    const searchQuery = "PUT A SEARCH TERM HERE TO SEARCH ON ❌VIDEOS";
    
    let res = await axios.get("https://fantox001-scrappy-api.vercel.app/xvideos?search=" + searchQuery)
    
    const scrappedURL = res.data.videoUrl
    
    console.log(scrappedURL)
  }
  
  main();
  
```

<br>

- In WhatsApp bot or any other bots:
```
// Note: Bot's code definition will vary from one bot to another. So please use it according to your bot's code.

const axios = require("axios");
const searchQuery = args.join(" ");

if(!searchQuery){
  return reply('Please provide a ❌videos search term to get video!');
}

let res = await axios.get("https://fantox001-scrappy-api.vercel.app/xvideos?search=" + searchQuery)

const scrappedURL = res.data.videoUrl

// Send video through scrapped link
await client.sendMessage( m.chat,{ video: { url: scrappedURL }, caption: `_Scrappy API by: FantoX001_` },{ quoted: m });
  
```


