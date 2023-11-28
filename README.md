# Rule

> 免责声明：该项目仅供个人学习、交流，请勿用于非法用途，请勿用于生产环境  

## Apple CDN
- 描述：规则组包含 Apple, Inc. 在中华人民共和国完成工信部 ICP 备案和公安网备、且在中华人民共和国境内提供 HTTP 服务的域名，如果由于某些原因需要代理其中部分域名，请自行针对域名编写规则、并添加到当前规则组之前。
- 数据来源 felixonmars/dnsmasq-china-list

### Surge
```
DOMAIN-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/apple_cdn.conf,[Replace with your policy]
```
### Clash
```
rule-providers:
  apple_cdn:
    type: http
    behavior: domain
    format: text
    interval: 43200
    url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/apple_cdn.txt
    path: ./Rules/apple_cdn.txt

rules:
  - RULE-SET,apple_cdn,[Replace with your policy]
```

## Global Stream
- 描述：包含 4gtv、AbemaTV、All4、Amazon Prime Video、Apple TV、Apple Music TV、Bahamut、BBC、Bilibili Intl、DAZN、Deezer、Disney+、Discovery+、DMM、encoreTVB、Fox Now、Fox+、HBO GO/Now/Max/Asia、Hulu、HWTV、JOOX、Jwplayer、KKBOX、KKTV、Line TV、Naver TV、myTV Super、Netflix、niconico、Now E、Paramount+、PBS、Peacock、Pandora、PBS、Pornhub、SoundCloud、PBS、Spotify、TaiwanGood、Tiktok Intl、Twitch、ViuTV、ShowTime、iQiYi Global、Himalaya Podcast、Overcast、WeTV 的规则组

### Surge
```
RULE-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/stream.conf,[Replace with your policy]
RULE-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/stream_ip.conf,[Replace with your policy]
```
### Clash
```
rule-providers:
  stream:
    type: http
    behavior: classical
    format: text
    interval: 43200
    url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/stream.conf
    path: ./Rules/stream.txt
  stream_ip:
    type: http
    behavior: classical
    format: text
    interval: 43200
    url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/stream_ip.conf
    path: ./Rules/stream_ip.txt

rules:
  - RULE-SET,stream,[Replace with your policy]
  - RULE-SET,stream_ip,[Replace with your policy]
```
