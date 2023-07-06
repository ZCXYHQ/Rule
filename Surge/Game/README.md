# 🧸 游戏

## 前言

![](https://shields.io/badge/-移除重复规则-ff69b4) ![](https://shields.io/badge/-DOMAIN与DOMAIN--SUFFIX合并-green) ![](https://shields.io/badge/-DOMAIN--SUFFIX间合并-critical) ![](https://shields.io/badge/-DOMAIN--SUFFIX与DOMAIN--KEYWORD合并-blue) ![](https://shields.io/badge/-IP--CIDR(6)合并-blueviolet) 

分流规则是互联网公共服务的域名和IP地址汇总，所有数据均收集自互联网公开信息，不代表我们支持或使用这些服务。

请通过【中华人民共和国 People's Republic of China】合法的互联网出入口信道访问规则中的地址，并确保在使用过程中符合相关法律法规。

## 规则说明
含有Steam、Blizzard、Discord、Rockstar等分流规则

## 规则统计

最后更新时间：2023-07-06 17:49:40

各类型规则统计：
| 类型 | 数量(条)  | 
| ---- | ----  |
| DOMAIN | 13  | 
| DOMAIN-KEYWORD | 4  | 
| DOMAIN-SUFFIX | 525  | 
| IP-CIDR | 46  | 
| PROTOCOL | 1  | 
| TOTAL | 589  | 


## Surge 

#### 使用说明
- Game.list，请使用RULE-SET。
- Game_Resolve.list，请使用RULE-SET。

#### 文件区别
- Game_Resolve.list与Game.list的区别仅在于后者IP-CIDR(6)类型带no-resolve。

#### 配置建议
- Game.list 单独使用。
- Game_Resolve.list 单独使用。

#### 规则链接
**MASTER分支

https://raw.githubusercontent.com/ZCXYHQ/Rule/main/Surge/Game/Game.list

**MASTER分支 CDN

https://cdn.jsdelivr.net/gh/ZCXYHQ/Rule@master/Surge/Game/Game.list

## 子规则/排除规则

当前分流规则，已包含以下子规则，除非特殊需求否则不建议重复引用：
| 子规则  |  |  |  |  | 
| ---- | ---- | ---- | ---- | ----  |
| Battle | Blizzard | Classic | DiabloIII | EA  | 
| Epic | Garena | Gog | Hearthstone | HeroesoftheStorm  | 
| Nintendo | OP | Overwatch | PlayStation | Purikonejp  | 
| Riot | Rockstar | StarCraftII | Steam | SteamCN  | 
| Supercell | UBI | WildRift | WorldofWarcraft | Xbox  | 

