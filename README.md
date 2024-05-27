# Floppa: Function-Calling Language Model as Portable Private Assistant

## Tool Pool

| user intention      | service provider                             | notes                                              |
|---------------------|----------------------------------------------|----------------------------------------------------|
| get date / time     | built-in                                     |                                                    |
| get location        | built-in, geo data api                       | location to coordinates or reverse                 |
| selection           | built-in                                     | select from list, forward/backward, last/next page |
| translate           | google  translate                            |                                                    |
| get weather         | open weather, yahoo weather, weather api     |                                                    |
| common search       | google, duckduckgo, baidu                    |                                                    |
| social media search | twitter, wechat platform, weibo, xiaohongshu | select provider based on search query              | 
| routing             | fast-routing                                 |                                                    |
| map                 | google maps                                  |                                                    | 
| local life          | google maps, yelp                            |                                                    | 
| trending news       | google, weibo, baidu                         |                                                    |
| events              | google                                       |                                                    |
| railway info        | china train                                  |                                                    | 
| travel              | flight radar, trip advisor, travel advisor   |                                                    |
| shopping            | tmall, jd, pinduoduo, 1688                   |                                                    | 
| information         | social presence checking, whois              |                                                    | 
| video               | tiktok, youtube                              |                                                    | 
| music               | spotify, billboard, lyrics                   |                                                    | 
| writing             | grammar checking, dictionary, rephrase       |                                                    | 


## Rapid API wrapping (V2)

| api name               | api description link                                                                   |
|------------------------|----------------------------------------------------------------------------------------| 
| Trueway GeoCoding      | https://rapidapi.com/trueway/api/trueway-geocoding/                                    |
| Google Translate       | https://rapidapi.com/googlecloud/api/google-translate1/                                | 
| OpenWeather            | https://rapidapi.com/worldapi/api/open-weather13/                                      | 
| Google Search          | https://rapidapi.com/herosAPI/api/google-search74                                      | 
| DuckDuckGo             | https://rapidapi.com/epctex-epctex-default/api/duckduckgo10/                           | 
| Wechat Search          | https://rapidapi.com/dataapiman/api/weixin-wechat-official-accounts-platform/          |
| Weibo                  | https://rapidapi.com/dataapiman/api/weibo-all-api/                                     | 
| Xiaohongshu            | https://rapidapi.com/dataapiman/api/xiaohongshu-all-api/                               | 
| Fast Routing           | https://rapidapi.com/Routing/api/fast-routing/                                         | 
| Google Maps Data       | https://rapidapi.com/alexanderxbx/api/maps-data/                                       | 
| Local Business         | https://rapidapi.com/letscrape-6bRBa3QguO5/api/local-business-data/                    | 
| Yelp                   | https://rapidapi.com/hannahle/api/yelp-com/                                            | 
| Google News            | https://rapidapi.com/bfd-id/api/google-news13/                                         | 
| NewsAPI                | https://rapidapi.com/strataconsultingllc/api/newsapi90/                                | 
| Weibo Trending         | https://rapidapi.com/wodezhanghaozhijia/api/top-trending-topics-on-weibo-china-twiter/ | 
| Baidu Trending         | https://rapidapi.com/wodezhanghaozhijia/api/top-trending-topics-on-baidu-china-google/ | 
| China Train/Rail       | https://rapidapi.com/etcloud-etcloud-default/api/china-train-rail/                     | 
| TripAdvisor            | https://rapidapi.com/DataCrawler/api/tripadvisor16/                                    | 
| Taobao Data Service    | https://rapidapi.com/ShowApi/api/taobao-tmall-data-service/                            | 
| JD Data Service        | https://rapidapi.com/ShowApi/api/jd-com-data-service/                                  | 
| Pinduoduo Data Service | https://rapidapi.com/ShowApi/api/pinduoduo-data-service/                               | 

## Built-In Python Code (V1)

Datetime (current time, time conversion, timezone calculation, time delta calculation)
Calculator
Stats (mean, min, max, ...)
Sort 


## VirtualScreenAgent




## Continue Pre-train 


## SFT format

```
<|im_start|>user
xxxxxx
<|im_end|>
<|im_start|>assistant
xxxxxx <|fc_start|><intention_slot_i><provider_slot_2>arg1=v1, arg2=v2<|fc_end|>

```

```
<|im_start|>user
xxxxxx
<|im_end|>
<|im_start|>assistant
xxxxxx <|fc_response_start|>xxxxxxxxxx<|fc_response_end|> xxxxxxxxxxxx
<|im_end|>
```