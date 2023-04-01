<h1 align="center">Scrappy API</a>
</h1>

<h4 align="center">A 4 in 1 scraper API with Genius Lyrics, Instagram, Facebook and ❌videos scraper coded by FantoX powerded by <a href="https://nodejs.org/en">Node.js</a>, <a href="https://expressjs.com/">Express.js</a> and <a href="https://vercel.com/">Vercel.com</a> free hosting.
</h4>

<p align="center">
<a href="#"><img title="Rest-Api" src="https://img.shields.io/badge/Rest Api-green?colorA=%23ff0000&colorB=%23017e40&style=for-the-badge"></a>
</p>


<p align="center">
<a href="https://github.com/FantoX001/Scrappy-API"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FFantoX001%2FScrappy-API&count_bg=%23FFA305&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Total+Hits&edge_flat=false)](https://hits.seeyoufarm.com" width="150px" /></a>
</p>

<p align="center">
<a href="https://github.com/FantoX001"><img title="Author" src="https://img.shields.io/badge/Developer-FantoX001-orange.svg?style=for-the-badge&logo=github" width="180px"></a>


<p align="center">
<a href="https://github.com/FantoX001/Scrappy-API"><img title="Open Source" src="https://img.shields.io/badge/Free%20To%20Use-YES-green.svg?style=for-the-badge" width="140px"></a>
<a href="https://github.com/FantoX001/Scrappy-API"><img title="" src="https://img.shields.io/badge/Maintained-Yes-green.svg?style=for-the-badge" width="140px"></a>
</p>
  
</p>

<br>

## 🧩 Install dependencies:

<h3><b>Using Node Package Manager (NPM): </b></h3>

```
npm i axios
```
<h3><b>Using Yet Another Resource Negotiator (YARN): </b></h3>

```
yarn add axios
```

<br>

## 🎀 API Endpoints & Usage:

<h3><b>Endpoints: </b></h3>

```
https://fantox001-scrappy-api.vercel.app/fbdl?url=PUT PUBLIC FACEBOOK VIDEO URL HERE
```

```
https://fantox001-scrappy-api.vercel.app/instadl?url=PUT PUBLIC INSTAGRAM VIDEO/REEL URL HERE
```

```
https://fantox001-scrappy-api.vercel.app/lyrics?search=PUT A SHORT SONG NAME
```

```
https://fantox001-scrappy-api.vercel.app/xvideos?search=PUT A ❌videos SEARCH TERM
```

<br>

<h2 align="center">📥 Facebook video scraper:
</h2>


<h3><b>Normal use: </b></h3>

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

<h3><b>In WhatsApp bots: </b></h3>

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

<h3><b>Normal use: </b></h3>

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

<h3><b>In WhatsApp bots: </b></h3>

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


<h3><b>Normal use: </b></h3>

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

<h3><b>In WhatsApp bots: </b></h3>

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

<h3><b>Normal use: </b></h3>

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

<h3><b>In WhatsApp bots: </b></h3>

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


