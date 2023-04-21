
<p align="center">
<a href="https://github.com/FantoX001/Scrappy-API">
 <img src="https://graph.org/file/70d6fe948789912152a54.png">

  </a>
 </p>


<h1 align="center">Scrappy API</a>
</h1>

<h3 align="center">A 6 in 1 scraper API with Genius Lyrics, Tech news ( gadgets360.com ), Tech News Random ( gadgets360.com random news page ), Instagram, Facebook and ❌videos scraper coded by <a href="https://github.com/FantoX001">FantoX</a> powered by <a href="https://nodejs.org/en">Node.js</a>, <a href="https://expressjs.com/">Express.js</a> and <a href="https://vercel.com/">Vercel.com</a> free hosting.
</h3>

<h3 align="center">Scrappy - The first Made in India Facebook and Instagram Scraper API.
 </h3>

<p align="center">
<a href="#"><img title="Rest-Api" src="https://img.shields.io/badge/Rest Api-green?colorA=%23ff0000&colorB=%23017e40&style=for-the-badge"></a>
</p>


<p align="center">
<a href="https://github.com/FantoX001/Scrappy-API"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FFantoX001%2FScrappy-API&count_bg=%23FFA305&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Total+Hits&edge_flat=false)](https://hits.seeyoufarm.com" width="150px" /></a>
</p>

<p align="center">
<a href="https://github.com/FantoX001"><img title="Author" src="https://img.shields.io/badge/Developer-FantoX001-white.svg?style=for-the-badge&logo=github" width="180px"></a>


<p align="center">
<a href="https://github.com/FantoX001/Scrappy-API"><img title="Open Source" src="https://img.shields.io/badge/Free%20To%20Use-YES-green.svg?style=for-the-badge" width="140px"></a>
<a href="https://github.com/FantoX001/Scrappy-API"><img title="" src="https://img.shields.io/badge/Maintained-Yes-green.svg?style=for-the-badge" width="140px"></a>
</p>
  
</p>

<br>

## 🧩 Install dependencies:

<h3><b>Using NPM: </b></h3>

```
npm i axios
```
<h3><b>Using YARN: </b></h3>

```
yarn add axios
```

<br>

## 🎀 API Endpoints & Usage:

<h3><b>Endpoints: </b></h3>


```
https://fantox001-scrappy-api.vercel.app/technews
```

```
https://fantox001-scrappy-api.vercel.app/technews/random
```

```
https://fantox001-scrappy-api.vercel.app/lyrics?search=PUT A SHORT SONG NAME
```

```
https://fantox001-scrappy-api.vercel.app/xvideos?search=PUT A ❌videos SEARCH TERM
```

```
https://fantox001-scrappy-api.vercel.app/fbdl?url=PUT PUBLIC FACEBOOK VIDEO URL HERE
```

```
https://fantox001-scrappy-api.vercel.app/instadl?url=PUT PUBLIC INSTAGRAM VIDEO/REEL URL HERE
```



<br>

<h2 align="center">📥 Facebook video scraper V2
</h2>


<h3><b>Normal use: </b></h3>

```js
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

```js
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

<h2 align="center">🎬 Instagram video scraper
</h2>

<h3><b>Normal use: </b></h3>

```js
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

```js
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

<h2 align="center">📜 Tech news scraper (Array response)
</h2>


<h3><b>Normal use: </b></h3>

```js
const axios = require("axios");

async function main() {

    const newsArray = await axios.get("https://fantox001-scrappy-api.vercel.app/technews")
    const allNews = newsArray.data;
    // This following code will Scrap and return an array of updated tech news including it's title, and Url

    console.log(allNews);
    // Now you can use that in any way you want by it's index number
  }
  
  main();
  
```

<br>

<h3><b>Raw API Response Example:</b></h3>

```
[
  {
    title: 'No Blue Tick for Pope as Twitter Cuts ‘Legacy’ Checks; Musk ‘Pays’ to Keep LeBron James, Stephen King Verified',
    link: 'https://www.gadgets360.com/apps/news/elon-musk-twitter-blue-tick-legacy-verified-accounts-stephen-king-lebron-james-pope-3966918'
  },
  {
    title: 'SpaceX Starship Explodes Minutes After Liftoff; Elon Musk Says ‘Learned a Lot’',
    link: 'https://www.gadgets360.com/science/news/elon-musk-spacex-starship-rocket-explodes-minutes-after-liftoff-launch-space-test-flight-3966826'
  },
  {
    title: 'ZTE Axon 40 Lite With Unisoc T616, 50-Megapixel Camera Launched: Price, Specifications',
    link: 'https://www.gadgets360.com/mobiles/news/zte-axon-40-lite-price-mxn-3999-launch-sale-date-specifications-features-3965555'
  },
  {
    title: "European Parliament Backs EU's First Set of Regulations for Crypto Assets; Rules to Roll Out in 2024",
    link: 'https://www.gadgets360.com/cryptocurrency/news/eu-parliament-backs-comprehensive-rules-for-crypto-assets-bitcoin-3965346'
  },
  {
    title: 'Poco F5 India Launch Teased, RAM and Storage Configurations Revealed: All Details',
    link: 'https://www.gadgets360.com/mobiles/news/poco-f5-india-launch-teaser-himanshu-tandon-ram-storage-configurations-twitter-3965147'
  },
  {
    title: 'Indian Automobile Tycoon Anand Mahindra Hints at Considering Bitcoin Payments for Cars',
    link: 'https://www.gadgets360.com/cryptocurrency/news/anand-mahindra-hints-considering-bitcoin-payments-cars-automobile-3965301'
  },
  {
    title: "Michael Schumacher's Family Planning Legal Action Against German Magazine Over AI-Generated Interview",
    link: 'https://www.gadgets360.com/internet/news/michael-schumacher-family-planning-legal-action-ai-interview-3965276'
  },
  {
    title: 'OnePlus Nord N30 Spotted on Google Play Console, Could Be Powered by Snapdragon 695 SoC: Report',
    link: 'https://www.gadgets360.com/mobiles/news/oneplus-nord-n30-specifications-tipped-google-pay-console-listing-report-3965234'
  },
  {
    title: 'Irrfan Khan’s The Song of Scorpions Sets April Release Date in India',
    link: 'https://www.gadgets360.com/entertainment/news/irrfan-khan-song-of-scorpions-movie-release-date-india-trailer-golshifteh-farahani-panorama-spotlight-3965210'
  },
  {
    title: 'TSMC Forecasts Up to 16 Percent Drop in Q2 Sales Amid Struggles to Clear Inventory, Weak Global Economy',
    link: 'https://www.gadgets360.com/mobiles/news/tsmc-q2-2023-forecast-sales-fall-16-percent-weak-global-economy-inventory-clearance-3965127'
  },
  {
    title: "Zee5's New Fantasy Series Fireflies: Parth Aur Jugnu to Stream May 5",
    link: 'https://www.gadgets360.com/entertainment/news/fireflies-parth-aur-jugnu-release-date-web-series-cast-meet-mukhi-aekam-binjwe-zee5-3965022'
  },
  {
    title: 'Cybersecurity, IP Theft and Accidents Top Three Threats to Indian Industry, Survey Shows',
    link: 'https://www.gadgets360.com/internet/news/cybersecurity-ip-theft-accidents-india-risk-survey-industry-vulnerabilities-3964956'
  },
  {
    title: 'Google Pixel Tablet Price Leaked Online, Tipped to Come in Two Colourways',
    link: 'https://www.gadgets360.com/tablets/news/google-pixel-tablet-price-eur-600-650-launch-specification-leak-3964741'
  },
  {
    title: 'Redmi Note 12 Pro 5G, Redmi Note 12 Pro+ 5G Get Android 12-Based MIUI 14 OS Update: All Details',
    link: 'https://www.gadgets360.com/mobiles/news/redmi-note-12-pro-plus-5g-android-12-miui-14-update-new-features-improvements-3964692'
  },
  {
    title: 'Samsung Galaxy F54 5G Reportedly Spotted on Google Play Console; Specifications Tipped',
    link: 'https://www.gadgets360.com/mobiles/news/samsung-f54-5g-google-play-console-specifications-india-launch-galaxy-3964674'
  },
  {
    title: 'BTC, ETH Record Notable Losses After Period of Surge, Crypto Market Plunges by Over 4 Percent',
    link: 'https://www.gadgets360.com/cryptocurrency/news/bitcoin-price-today-ether-altcoin-crypto-market-down-3964671'
  },
  {
    title: 'Sanya Malhotra’s Kathal – a Jackfruit Mystery Sets May 19 Release Date on Netflix',
    link: 'https://www.gadgets360.com/entertainment/news/kathal-movie-release-date-cast-sanya-malhotra-rajpal-yadav-ott-stream-netflix-3964655'
  },
  {
    title: 'Apple’s Recent iOS 16.4.1 Update Reportedly Leaves iPhones Overheated: Why You Should Update Anyway',
    link: 'https://www.gadgets360.com/mobiles/news/ios-16-4-1-update-iphone-overheating-issue-fixes-security-flaws-vulnerabilities-3964648'
  },
  {
    title: 'National Quantum Mission Worth Rs. 6,003 Crore Approved By Union Cabinet: Details',
    link: 'https://www.gadgets360.com/internet/news/national-quantum-mission-approved-rs-6003-crore-research-development-communications-technology-3964501'     
  },
  {
    title: 'Elon Musk Threatens Lawsuit After Microsoft Removes Twitter From Ad Platform',
    link: 'https://www.gadgets360.com/social-networking/news/elon-musk-lawsuit-threat-twitter-removed-microsoft-ad-platform-illegal-use-training-data-3964412'  
  }
]
```

<br><br>

<h2 align="center">💻 Random Tech news scraper
</h2>


<h3><b>Normal use: </b></h3>

```js
const axios = require("axios");

async function main() {

    const mainNews = await axios.get("https://fantox001-scrappy-api.vercel.app/technews/random")
    const mainData = mainNews.data;
    // This following code will Scrap a random news from `gadgets360.com` and return it's Full News and Thumbnail.

    // Separating the News and Thumbnail.
    const news = mainData.news;
    const thumbnail = mainData.thumbnail;

    console.log(news); // This is Full News
    console.log(thumbnail); // This is Thumbnail of that News

  }
  
  main();
  
```

<br>

<h3><b>Raw API Response Example ( Without formatting ):</b></h3>

```
{
  status: 'Scraping is successful!',
  credit: 'Scrappy - Coded by @FantoX001 - All rights reserved',
  news: `Intellectual property theft, information and cyber security threats and accidents have been ranked as the top three threats in India by the industry in a risk survey, according to a FICCI report.Also, 'threat to women safety' risk has jumped from 12th place in 2021 to 5th place in 2022 India Risk Survey, the report stated while urging companies to take measures to ensure the safety of their women employees. According to respodents, the lowest risk is associated with terrorism and insurgency, the report released on Wednesday said.Among sectors, logistics and construction segments have highlighted accidents and intellectual property theft as major "risks" facing them."For the logistic sector, accidents are their second major concern as transportation is more prone to road accidents, while intellectual property theft has been placed at number one by the respondents. Likewise, the construction industry has voted accidents on the top position as the construction sites face a lot of challenges in combating accidents," the 'India Risk Survey' of FICCI said.The survey identifies 12 key areas of concern for businesses and five emerging risks that might seriously damage India's business ecosystem.The annual survey aims to identify potential risks in the context of a changing global environment, allowing business leaders to assess their circumspection for disruptive events like rapid digitalization, accidents, and business espionage, in the future and to ameliorate risk mitigation techniques.India's retail industry ranked accidents, intellectual property theft and natural hazards as its prime issues.The media and entertainment industry has marked information and cyber insecurity, business espionage and fire incidents as major threats.For information & technology (IT) and manufacturing industry intellectual property theft is one of the top risks, while the consulting sector has placed business espionage in the second spot after cyber insecurity.Other sectors which posed issues like accidents, intellectual property theft, business espionage among others as major risks are real estate, education, security services, financial services and hospitality.`,
  thumbnail: 'https://i.gadgets360cdn.com/large/cybersecurity_unsplash_1681991423295.jpg?downsize=950:*'
}
```


<br><br>

<h2 align="center">🎼 Genius Lyrics scraper
</h2>


<h3><b>Normal use: </b></h3>

```js
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

```js
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

<h2 align="center">❌videos scraper
</h2>

<h3><b>Normal use: </b></h3>

```js
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

```js
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

## 📛 Frequently asked questions:

Q. Why source code of this API is not public ?
- Scraping is in other words stealing data from an website without permission. Also almost no websites allows it as it puts extra load on their servers. So with respect to their policies I didn't made the source code public.

Q. Will you sell this source code for money ?
- No, I don't work for money. As a node.js lover, I only work for fun or experiment.
