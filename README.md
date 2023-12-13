# Rule

> 免责声明：该项目仅供个人学习、交流，请勿用于非法用途，请勿用于生产环境  

## Apple Service
- 描述：该文件包含Apple,Inc在中国大陆没有PoP的域名。
### Surge
```
RULE-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Apple_Service.conf,[Replace with your policy]
```
### Clash
```
rule-providers:
    Apple_Services:
      type: http
      behavior: classical
      path: ./Rules/Apple_Services.yaml
      url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Apple_Service.yaml
      interval: 43200

rules:
  - RULE-SET,Apple_Services,[Replace with your policy]
```

## Global Stream
- 人工维护
- 描述：规则组包含AbemaTV、Amazon Prime Video、Apple TV、Apple Music TV、Bahamut、BBC、Bilibili International、DAZN、Disney+、Discovery+、DMM、E-Hentai、HBO Asia、Hulu、iQiYi Global、KKTV、Max、myTV Super、Netflix、niconico、Now E、Paramount+、Pornhub、Spotify、TikTok、TVB Anywhere、Twitch、ViuTV

### Surge
```
RULE-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Stream.conf,[Replace with your policy]
RULE-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Stream_IP.conf,[Replace with your policy]
```
### Clash
```
rule-providers:
    Stream:
      type: http
      behavior: classical
      path: ./Rules/Stream.yaml
      url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Clash/Stream.yaml
      interval: 43200
    Stream_IP:
      type: http
      behavior: classical
      path: ./Rules/Stream_IP.yaml
      url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Clash/Stream_IP.yaml
      interval: 43200

rules:
  - RULE-SET,Stream,[Replace with your policy]
  - RULE-SET,Stream_IP,[Replace with your policy]
```
