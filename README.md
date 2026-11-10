# YouTube 视频帖子抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/youtube) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/youtube) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![推广](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/youtube)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的 YouTube 视频帖子数据。**

此代码库提供两种大规模访问 YouTube 视频帖子数据的方法：

- **[方法 1：Bright Data YouTube 视频帖子爬虫工具 API](#方法-1bright-data-youtube-视频帖子爬虫工具-api)**（推荐）- 完全托管的企业级抓取 API，可自动处理代理、CAPTCHA 和扩展。
- **[方法 2：Bright Data YouTube 视频帖子数据集](#方法-2bright-data-youtube-视频帖子数据集)** - 可直接下载的预采集 YouTube 视频帖子数据集，无需爬虫。

## 目录

- [为什么使用 Bright Data 抓取 YouTube 视频帖子？](#为什么使用-bright-data-抓取-youtube-视频帖子)
- [方法 1：Bright Data YouTube 视频帖子爬虫工具 API](#方法-1bright-data-youtube-视频帖子爬虫工具-api)
  - [快速入门](#youtube-视频帖子爬虫工具-api-快速入门)
  - [1. YouTube 视频帖子数据](#1-youtube-视频帖子数据)
- [方法 2：Bright Data YouTube 视频帖子数据集](#方法-2bright-data-youtube-视频帖子数据集)
- [数据采集方式](#数据采集方式)

## 为什么使用 Bright Data 抓取 YouTube 视频帖子？

抓取 YouTube 视频帖子面临多项挑战：

- 速率限制：YouTube 会监控请求频率，并可能封禁超出限制的 IP。
- CAPTCHA 检测：自动访问可能会触发 CAPTCHA 验证。
- 身份验证障碍：部分数据需要登录才能访问，且平台会检测自动化尝试。
- 动态内容加载：使用简单的 HTTP 请求很难抓取由 JavaScript 渲染的内容。
- IP 封禁：从同一 IP 重复发送请求可能会导致封禁。

Bright Data 的 YouTube 视频帖子爬虫工具 API 可通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的速率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：接收可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：支持任意规模的云端托管抓取
- ✅ **99.9% 正常运行时间 SLA**：为业务关键型工作流提供可靠的数据采集

## 方法 1：Bright Data YouTube 视频帖子爬虫工具 API

[Bright Data YouTube 视频帖子爬虫工具 API](https://www.bright.cn/products/web-scraper/youtube) 是一种无需配置任何基础设施的完全托管解决方案。

### YouTube 视频帖子爬虫工具 API 快速入门

1. **注册**一个[免费的 Bright Data 账户](https://www.bright.cn/)
2. **前往** [YouTube 视频帖子爬虫工具 API](https://www.bright.cn/products/web-scraper/youtube)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `youtube-videos-posts_scraper_api_codes/` 中的任意脚本

### 1. YouTube 视频帖子数据

采集 YouTube 视频帖子数据。

#### 输入参数

| 字段 | 类型 | 必填 | 说明 |
|-------|------|----------|-------------|
| `url` | string | 是 | 要抓取的 YouTube 视频帖子项目 URL |
| `limit` | integer | 否 | 返回结果的最大数量 |
| `include_errors` | boolean | 否 | 在响应中包含错误详情 |
| `notify` | url | 否 | 采集完成时用于接收通知的 Webhook URL |
| `format` | enum | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "avatar_img_channel": "https://yt3.ggpht.com/MOWpaiGJdgN4aKMI-NGQLL4jMVP3aDORlQpOBWooi0GSE2TGt4_9ncyepk1pCh-yWQ795AhPbw=s48-c-k-c0x00ffffff-no-rj",
  "category": "Music",
  "channel_url": "https://www.youtube.com/@RickAstleyYT",
  "channel_url_decoded": "https://www.youtube.com/@RickAstleyYT",
  "codecs": "avc1.42001E, mp4a.40.2 / mp4a.40.2",
  "color": "bt709",
  "current_optimal_res": "640x360@25 / 640x360@25",
  "date_posted": "2009-10-25T06:57:33.000Z",
  "description": "The official video for \u201cNever Gonna Give You Up\u201d by Rick Astley. \n\nNever: The Autobiography \ud83d\udcda OUT NOW! \nFollow this link to get your copy and listen to Rick\u2019s \u2018Never\u2019 playlist \u2764\ufe0f #RickAstleyNever\nhttps://linktr.ee/rickastleynever\n\n\u201cNever Gonna Give You Up\u201d was a global smash on its release in July 1987, topping the charts in 25 countries including Rick\u2019s native UK and the US Billboard Hot 100.  It also won the Brit Award for Best single in 1988. Stock Aitken and Waterman wrote and produced the track which was the lead-off single and lead track from Rick\u2019s debut LP \u201cWhenever You Need Somebody\u201d.  The album was itself a UK number one and would go on to sell over 15 million copies worldwide.\n\nThe legendary video was directed by Simon West \u2013 who later went on to make Hollywood blockbusters such as Con Air, Lara Croft \u2013 Tomb Raider and The Expendables 2.  The video passed the 1bn YouTube views milestone on 28 July 2021.\n\nSubscribe to the official Rick Astley YouTube channel: https://RickAstley.lnk.to/YTSubID\n\nFollow Rick Astley:\nFacebook: https://RickAstley.lnk.to/FBFollowID \nTwitter: https://RickAstley.lnk.to/TwitterID \nInstagram: https://RickAstley.lnk.to/InstagramID \nWebsite: https://RickAstley.lnk.to/storeID \nTikTok: https://RickAstley.lnk.to/TikTokID\n\nListen to Rick Astley:\nSpotify: https://RickAstley.lnk.to/SpotifyID \nApple Music: https://RickAstley.lnk.to/AppleMusicID \nAmazon Music: https://RickAstley.lnk.to/AmazonMusicID \nDeezer: https://RickAstley.lnk.to/DeezerID \n\nLyrics:\nWe\u2019re no strangers to love\nYou know the rules and so do I\nA full commitment\u2019s what I\u2019m thinking of\nYou wouldn\u2019t get this from any other guy\n\nI just wanna tell you how I\u2019m feeling\nGotta make you understand\n\nNever gonna give you up\nNever gonna let you down\nNever gonna run around and desert you\nNever gonna make you cry\nNever gonna say goodbye\nNever gonna tell a lie and hurt you\n\nWe\u2019ve known each other for so long\nYour heart\u2019s been aching but you\u2019re too shy to say it\nInside we both know what\u2019s been going on\nWe know the game and we\u2019re gonna play it\n\nAnd if you ask me how I\u2019m feeling\nDon\u2019t tell me you\u2019re too blind to see\n\nNever gonna give you up\nNever gonna let you down\nNever gonna run around and desert you\nNever gonna make you cry\nNever gonna say goodbye\nNever gonna tell a lie and hurt you\n\n#RickAstley #NeverGonnaGiveYouUp #WheneverYouNeedSomebody #OfficialMusicVideo",
  "formatted_transcript": [
    {
      "duration": 17000,
      "end_time": 18000,
      "start_time": 1000,
      "text": "[\u266a\u266a\u266a]"
    },
    {
      "duration": 9000,
      "end_time": 27000,
      "start_time": 18000,
      "text": "\u266a We\u0027re no strangers to love \u266a \u266a You know the rules and so do I \u266a"
    },
    {
      "duration": 8000,
      "end_time": 35000,
      "start_time": 27000,
      "text": "\u266a A full commitment\u0027s what I\u0027m thinking of \u266a \u266a You wouldn\u0027t get this from any other guy \u266a"
    },
    {
      "duration": 8000,
      "end_time": 43000,
      "start_time": 35000,
      "text": "\u266a I just wanna tell you how I\u0027m feeling \u266a \u266a Gotta make you understand \u266a"
    },
    {
      "duration": 8000,
      "end_time": 51000,
      "start_time": 43000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 60000,
      "start_time": 51000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 69000,
      "start_time": 60000,
      "text": "\u266a We\u0027ve known each other for so long \u266a \u266a Your heart\u0027s been aching but you\u0027re too shy to say it \u266a"
    },
    {
      "duration": 8000,
      "end_time": 77000,
      "start_time": 69000,
      "text": "\u266a Inside we both know what\u0027s been going \u266a \u266a We know the game and we\u0027re gonna play it \u266a"
    },
    {
      "duration": 8000,
      "end_time": 85000,
      "start_time": 77000,
      "text": "\u266a And if you ask me how I\u0027m feeling \u266a \u266a Don\u0027t tell me you\u0027re too blind to see \u266a"
    },
    {
      "duration": 8000,
      "end_time": 93000,
      "start_time": 85000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 102000,
      "start_time": 93000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    },
    {
      "duration": 8000,
      "end_time": 110000,
      "start_time": 102000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 119000,
      "start_time": 110000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 128000,
      "start_time": 119000,
      "text": "\u266a (Ooh, give you up) \u266a \u266a (Ooh, give you up) \u266a"
    },
    {
      "duration": 8000,
      "end_time": 136000,
      "start_time": 128000,
      "text": "\u266a Never gonna give, never gonna give \u266a \u266a (Give you up) \u266a \u266a Never gonna give, never gonna give \u266a \u266a (Give you up) \u266a"
    },
    {
      "duration": 9000,
      "end_time": 145000,
      "start_time": 136000,
      "text": "\u266a We\u0027ve known each other for so long \u266a \u266a Your heart\u0027s been aching but you\u0027re too shy to say it \u266a"
    },
    {
      "duration": 8000,
      "end_time": 153000,
      "start_time": 145000,
      "text": "\u266a Inside we both know what\u0027s been going \u266a \u266a We know the game and we\u0027re gonna play it \u266a"
    },
    {
      "duration": 8000,
      "end_time": 161000,
      "start_time": 153000,
      "text": "\u266a I just wanna tell you how I\u0027m feeling \u266a \u266a Gotta make you understand \u266a"
    },
    {
      "duration": 8000,
      "end_time": 169000,
      "start_time": 161000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 178000,
      "start_time": 169000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    },
    {
      "duration": 8000,
      "end_time": 186000,
      "start_time": 178000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 9000,
      "end_time": 195000,
      "start_time": 186000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    },
    {
      "duration": 8000,
      "end_time": 203000,
      "start_time": 195000,
      "text": "\u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a"
    },
    {
      "duration": 5000,
      "end_time": 208000,
      "start_time": 203000,
      "text": "\u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a"
    }
  ],
  "handle_name": "Rick Astley",
  "hashtags": [
    {
      "hashtag": "#RickAstley",
      "link": "https://www.youtube.com/hashtag/rickastley"
    },
    {
      "hashtag": "#NeverGonnaGiveYouUp",
      "link": "https://www.youtube.com/hashtag/nevergonnagiveyouup"
    },
    {
      "hashtag": "#OfficialMusicVideo",
      "link": "https://www.youtube.com/hashtag/officialmusicvideo"
    }
  ],
  "is_age_restricted": false,
  "is_sponsored": false,
  "likes": 18972606,
  "music": {
    "artist": "Rick Astley",
    "song": "Never Gonna Give You Up (7\" Mix)"
  },
  "next_recommended_videos": [
    {
      "endMs": 212040,
      "startMs": 201451,
      "style": "CHANNEL",
      "thumbnail": "https://yt3.ggpht.com/MOWpaiGJdgN4aKMI-NGQLL4jMVP3aDORlQpOBWooi0GSE2TGt4_9ncyepk1pCh-yWQ795AhPbw=s400-c-k-c0x00ffffff-no-rj",
      "title": "Rick Astley, channel",
      "url": "https://www.youtube.com/channel/UCuAXFkgsw1L7xaCfnd5JJOw"
    },
    {
      "endMs": 212040,
      "startMs": 201451,
      "style": "VIDEO",
      "thumbnail": "https://i.ytimg.com/vi/qQDrqV5Hw4c/maxresdefault.jpg?sqp=-oaymwEmCIAKENAF8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGFggXyhlMA8=\u0026rs=AOn4CLBDFgN-ehq0DU9qYo5qdDhC4mg_sw",
      "title": "Rick Astley - Never : The Autobiography - Listen to the introduction of the Audiobook, video",
      "url": "https://www.youtube.com/watch?v=qQDrqV5Hw4c"
    },
    {
      "endMs": 212040,
      "startMs": 201451,
      "style": "VIDEO",
      "thumbnail": "https://i.ytimg.com/vi_webp/yi6fWPV6qXg/maxresdefault.webp",
      "title": "Rick Astley - The Reflection Tour 2026 - Trailer, video",
      "url": "https://www.youtube.com/watch?v=yi6fWPV6qXg"
    },
    {
      "endMs": 212040,
      "startMs": 201451,
      "style": "PLAYLIST",
      "thumbnail": "https://i.ytimg.com/vi_webp/zRVjZ2DJ9Cg/maxresdefault.webp",
      "title": "41 videos, Rick Astley: Official Music Videos",
      "url": "https://www.youtube.com/watch?v=zRVjZ2DJ9Cg\u0026list=PLlaN88a7y2_plecYoJxvRFTLHVbIVAOoc"
    }
  ],
  "post_type": "post",
  "preview_image": "https://i.ytimg.com/vi_webp/dQw4w9WgXcQ/maxresdefault.webp",
  "quality": "hd2160",
  "quality_label": "2160p",
  "recommended_videos": [
    {
      "thumbnail": "https://i.ytimg.com/vi/oRdxUFDoQe0/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLDXKCqpEHRwn0zeDIqaBBtLKxxzYQ",
      "title": "Michael Jackson - Beat It (Official 4K Video)",
      "url": "https://www.youtube.com/watch?v=oRdxUFDoQe0\u0026list=RDoRdxUFDoQe0\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/dlH1XxyJ8jM/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLB3dnx5cf9zLjIDWkJtN_jxIMCl4Q",
      "title": "Rick Astley Loves Nutella",
      "url": "https://www.youtube.com/watch?v=dlH1XxyJ8jM"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/izGwDsrQ1eQ/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLD1vkgmEhFfM8_9782EhZ_gj-gbrQ",
      "title": "George Michael - Careless Whisper (Official Video)",
      "url": "https://www.youtube.com/watch?v=izGwDsrQ1eQ\u0026list=RDizGwDsrQ1eQ\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/XEjLoHdbVeE/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLB9McjJ1prlqCIHMNlrT1SHrooF8w",
      "title": "ABBA - Gimme! Gimme! Gimme! (A Man After Midnight)",
      "url": "https://www.youtube.com/watch?v=XEjLoHdbVeE\u0026list=RDXEjLoHdbVeE\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/yPYZpwSpKmA/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLCgJt2_an7C_u4uNIF2n9cGD0N0Ig",
      "title": "Rick Astley - Together Forever (Official Video) [4K Remaster]",
      "url": "https://www.youtube.com/watch?v=yPYZpwSpKmA\u0026list=RDyPYZpwSpKmA\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/vulK0wDSc24/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLC9h7OrvrSQr9JUPxGxKPJ3hXgD-w",
      "title": "(fan-voted) top 100 most recognizable songs of all-time",
      "url": "https://www.youtube.com/watch?v=vulK0wDSc24\u0026list=RDvulK0wDSc24\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/h_D3VFfhvs4/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLDcngThRuKG_8s4Em9VP8nB7MhdxQ",
      "title": "Michael Jackson - Smooth Criminal (Official Video)",
      "url": "https://www.youtube.com/watch?v=h_D3VFfhvs4\u0026list=RDh_D3VFfhvs4\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/nsCIeklgp1M/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLDGW2umApn7bUf_BRQ_OrsRs6KFyw",
      "title": "Rick Astley - Never Gonna Give You Up | Glastonbury 2023",
      "url": "https://www.youtube.com/watch?v=nsCIeklgp1M\u0026list=RDnsCIeklgp1M\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/eNvUS-6PTbs/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLAgPzUIbx8nlKvUM9FuureslK9j3Q",
      "title": "Modern Talking - Cheri Cheri Lady (Official\u00a0Video)",
      "url": "https://www.youtube.com/watch?v=eNvUS-6PTbs\u0026list=RDeNvUS-6PTbs\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/ci6ZtPAN0PM/hqdefault.jpg?sqp=-oaymwEnCNACELwBSFryq4qpAxkIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB\u0026rs=AOn4CLAudBm3na6q7DLBtpRWSzM7T5DJ6w",
      "title": "RickRolled by an Ad...",
      "url": "https://www.youtube.com/watch?v=ci6ZtPAN0PM\u0026pp=0gcJCdQKAYcqIYzv"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/1E30uKYHiEk/hqdefault.jpg?sqp=-oaymwFBCNACELwBSFryq4qpAzMIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB8AEB-AG-B4AC0AWKAgwIABABGF4gZShAMA8=\u0026rs=AOn4CLBoc475_MFQN4RWwajrOoBcar3qrA",
      "title": "Never Gonna Mix You Up (Part 2) - Rick Astley",
      "url": "https://www.youtube.com/watch?v=1E30uKYHiEk\u0026list=RD1E30uKYHiEk\u0026start_radio=1\u0026pp=oAcB"
    },
    {
      "thumbnail": "https://i.ytimg.com/vi/tSi6Dn1H36Y/hqdefault.jpg?sqp=-oaymwFBCNACELwBSFryq4qpAzMIARUAAIhCGAHYAQHiAQoIGBACGAY4AUAB8AEB-AH-BIAC4AOKAgwIABABGGUgUihNMA8=\u0026rs=AOn4CLAsyG_u17r3nGnWVrz89W3lNUAIDA",
      "title": "Michael Jackson - Billie Jean (Live) - 1983",
      "url": "https://www.youtube.com/watch?v=tSi6Dn1H36Y\u0026list=RDtSi6Dn1H36Y\u0026start_radio=1\u0026pp=oAcB"
    }
  ],
  "shortcode": "dQw4w9WgXcQ",
  "subscribers": 4490000,
  "tags": [
    "rick astley",
    "Never Gonna Give You Up",
    "nggyu",
    "never gonna give you up lyrics",
    "rick rolled",
    "Rick Roll",
    "rick astley official",
    "rickrolled",
    "Fortnite song",
    "Fortnite event",
    "Fortnite dance",
    "fortnite never gonna give you up",
    "rick roll",
    "rickrolling",
    "rick rolling",
    "never gonna give you up",
    "80s music",
    "rick astley new",
    "animated video",
    "rickroll",
    "meme songs",
    "never gonna give u up lyrics",
    "Rick Astley 2022",
    "never gonna let you down",
    "animated",
    "rick rolls 2022",
    "never gonna give you up karaoke"
  ],
  "title": "Rick Astley - Never Gonna Give You Up (Official Video) (4K Remaster)",
  "transcript": "[\u266a\u266a\u266a] \u266a We\u0027re no strangers to love \u266a \u266a You know the rules and so do I \u266a \u266a A full commitment\u0027s what I\u0027m thinking of \u266a \u266a You wouldn\u0027t get this from any other guy \u266a \u266a I just wanna tell you how I\u0027m feeling \u266a \u266a Gotta make you understand \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a \u266a We\u0027ve known each other for so long \u266a \u266a Your heart\u0027s been aching but you\u0027re too shy to say it \u266a \u266a Inside we both know what\u0027s been going \u266a \u266a We know the game and we\u0027re gonna play it \u266a \u266a And if you ask me how I\u0027m feeling \u266a \u266a Don\u0027t tell me you\u0027re too blind to see \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a \u266a (Ooh, give you up) \u266a \u266a (Ooh, give you up) \u266a \u266a Never gonna give, never gonna give \u266a \u266a (Give you up) \u266a \u266a Never gonna give, never gonna give \u266a \u266a (Give you up) \u266a \u266a We\u0027ve known each other for so long \u266a \u266a Your heart\u0027s been aching but you\u0027re too shy to say it \u266a \u266a Inside we both know what\u0027s been going \u266a \u266a We know the game and we\u0027re gonna play it \u266a \u266a I just wanna tell you how I\u0027m feeling \u266a \u266a Gotta make you understand \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a \u266a Never gonna give you up \u266a \u266a Never gonna let you down \u266a \u266a Never gonna run around and desert you \u266a \u266a Never gonna make you cry \u266a \u266a Never gonna say goodbye \u266a \u266a Never gonna tell a lie and hurt you \u266a",
  "transcript_language": [
    {
      "auto_translate": false,
      "language": "English"
    },
    {
      "auto_translate": true,
      "language": "English (auto-generated)"
    },
    {
      "auto_translate": false,
      "language": "German (Germany)"
    },
    {
      "auto_translate": false,
      "language": "Japanese"
    },
    {
      "auto_translate": false,
      "language": "Portuguese (Brazil)"
    },
    {
      "auto_translate": false,
      "language": "Spanish (Latin America)"
    }
  ],
  "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "verified": false,
  "video_id": "dQw4w9WgXcQ",
  "video_length": 213,
  "video_url": "https://rr3---sn-xmjpuxa-qxak.googlevideo.com/videoplayback?expire=1777254214\u0026ei=5mruaYXeDd6-4t4P8ue1qQc\u0026ip=2401%3A9640%3A1%3A96d6%3A44cd%3A3445%3A5e35%3A18d\u0026id=o-AD-k-Kvbi7hOGIkOT_zoJtkraeYDM0ZBP8ZssB4JMiB1\u0026itag=18\u0026source=youtube\u0026requiressl=yes\u0026xpc=EgVo2aDSNQ%3D%3D\u0026cps=825\u0026met=1777232614%2C\u0026mh=7c\u0026mm=31%2C29\u0026mn=sn-xmjpuxa-qxak%2Csn-qxaeens6\u0026ms=au%2Crdu\u0026mv=m\u0026mvi=3\u0026pcm2cms=yes\u0026pl=48\u0026rms=au%2Cau\u0026initcwndbps=1911250\u0026bui=AUUZDGKuhUJFs9Sywdb8vYIgRMvldKx1HTcwDLUTRVvGEQXei2VDq87qc-SSCDneo7DbGkqTlKA6wshT\u0026spc=jlWavXDk3o3P1oCmZECuhSHevKe0s84IRvznvm4YmAOKeFVu-3SwRSamNwKhQO5XPFbIgmp9VtSI4w\u0026vprv=1\u0026svpuc=1\u0026mime=video%2Fmp4\u0026ns=De3XW03HBnJsV8PvseccYloU\u0026rqh=1\u0026cnr=14\u0026ratebypass=yes\u0026dur=213.089\u0026lmt=1766960953317159\u0026mt=1777232016\u0026fvip=3\u0026fexp=51565115%2C51565682%2C51869322\u0026c=WEB\u0026sefc=1\u0026txp=5538534\u0026n=eiaBLdFX6coQgvT\u0026sparams=expire%2Cei%2Cip%2Cid%2Citag%2Csource%2Crequiressl%2Cxpc%2Cbui%2Cspc%2Cvprv%2Csvpuc%2Cmime%2Cns%2Crqh%2Ccnr%2Cratebypass%2Cdur%2Clmt\u0026lsparams=cps%2Cmet%2Cmh%2Cmm%2Cmn%2Cms%2Cmv%2Cmvi%2Cpcm2cms%2Cpl%2Crms%2Cinitcwndbps\u0026lsig=APaTxxMwRQIgePLosJgBUcOUi4XAhYFPUCbz5OMHn9gaYLBdNia9za4CIQDVIFik1mcQVk94ugxFORRQKyUcb8mtK1gDr9nocvC3sA%3D%3D",
  "viewport_frames": "640x360 / -",
  "views": 1766281658,
  "youtuber": "@RickAstleyYT",
  "youtuber_id": "UCuAXFkgsw1L7xaCfnd5JJOw",
  "youtuber_md5": "4fc65cd6213b5c0f1d04c2aa3006f46a"
}
```

👉 查看[完整 Python 代码](youtube-videos-posts_scraper_api_codes/youtube_videos_posts_scraper.py)

## 方法 2：Bright Data YouTube 视频帖子数据集

如果你需要无需编写任何爬虫代码即可使用的数据，[Bright Data YouTube 视频帖子数据集](https://www.bright.cn/products/datasets/youtube)提供预先采集、定期更新且可立即下载的数据。

**为什么选择数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待采集
- 🔄 **定期更新**：按固定计划刷新最新数据
- 📊 **多种格式**：可下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖所有主要 YouTube 视频帖子类别的数百万条记录
- ✅ **完全合规**：数据来源符合道德规范并已通过法律审核

👉 **[探索 YouTube 视频帖子数据集](https://www.bright.cn/products/datasets/youtube)**

## 数据采集方式

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无 |
| 实时数据 | ✅ 是 | ❌ 预采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定架构 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| 验证码破解 | ✅ 自动 | N/A |
| 规模 | 无限制 | 无限制 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级 24/7 全天候支持 | 企业级 24/7 全天候支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/youtube](https://www.bright.cn/products/web-scraper/youtube)
