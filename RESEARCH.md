# Reverse Engineering thesession.org

BaseURL: https://thesession.org

# Search Query

https://thesession.org/ajax?url=https://thesession.org/tunes/search

with raw data 'type=@model=@q=@page=3

Full curl

[result of the search](query)

```
curl 'https://thesession.org/ajax?url=https://thesession.org/tunes/search' \
  -H 'accept: */*' \
  -H 'accept-language: en-US,en;q=0.9' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'origin: https://thesession.org' \
  -H 'priority: u=1, i' \
  -H 'sec-ch-ua: "Google Chrome";v="135", "Not-A.Brand";v="8", "Chromium";v="135"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-platform: "Windows"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/135.0.0.0 Safari/537.36' \
  -H 'x-requested-with: XMLHttpRequest' \
  --data-raw 'type=&mode=&q=&page=3'
```

# Tune linke

Simply https://thesession.org/tunes/713

[tune html](tune713.html)

Sheet music appears to be rendered with a library called [abcjs](https://github.com/paulrosen/abcjs)

There is an ABC tab with the abc music.  

midi is downloaded at /tunes/713/midi/1 (where last number is the song index)

abc is downloaded at /tunes/713/abc/1 (where last number is the song index.

)