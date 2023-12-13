# Rule

> 免责声明：该项目仅供个人学习、交流，请勿用于非法用途，请勿用于生产环境  

## Apple CDN
- 描述：规则组包含 Apple, Inc. 在中华人民共和国完成工信部 ICP 备案和公安网备、且在中华人民共和国境内提供 HTTP 服务的域名，如果由于某些原因需要代理其中部分域名，请自行针对域名编写规则、并添加到当前规则组之前。
- 数据来源 felixonmars/dnsmasq-china-list

### Surge
```
DOMAIN-SET,https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Apple_CDN.conf,[Replace with your policy]
```
### Clash
```
rule-providers:
    Apple_CDN:
      type: http
      behavior: domain
      path: ./Rules/apple_cdn.yaml
      url: https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@main/Surge/Apple_CDN.yaml
      interval: 43200

rules:
  - RULE-SET,Apple_CDN,[Replace with your policy]
```
## Apple Service
- 描述：该文件包含Apple, Inc.在中国大陆没有PoP的域名。
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
- 描述：规则组包含
```
- AbemaTV
- Amazon Prime Video
- Apple TV
- Apple Music TV
- Bahamut
- BBC
- Bilibili International
- DAZN
- Disney+
- Discovery+
- DMM
- E-Hentai
- HBO Asia
- Hulu
- iQiYi Global
- KKTV
- Max
- myTV Super
- Netflix
- niconico
- Now E
- Paramount+
- Pornhub
- Spotify
- TikTok
- TVB Anywhere
- Twitch
- ViuTV
```

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
