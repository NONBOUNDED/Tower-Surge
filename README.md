
; ============================================================
; 塔台 / Subconverter 远程规则模板
; 三机场节点由塔台负责合并；本文件只负责策略组 + 分流规则
; 基于用户原 Surge Pro (1).conf 重构
; ============================================================

[custom]

; =========================
; 基础开关
; =========================
enable_rule_generator=true
overwrite_original_rules=true

; =========================
; 节点策略组
; 塔台合并后的所有节点直接进入这些正则分组
; =========================

custom_proxy_group=🚀 节点选择`select`[]♻️ 自动选择`[]🚀 手动选择`[]🇭🇰 香港`[]🇨🇳 台湾`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🇺🇸 美国`[]🇰🇷 韩国`[]🇬🇧 英国`[]🇩🇪 德国`[]🇫🇷 法国`[]🇦🇺 澳洲`[]DIRECT

custom_proxy_group=♻️ 自动选择`url-test`(?i)^(?!.*(剩余|流量|套餐|到期|官网|重置|订阅|Expired|Remain|Reset)).+$`http://www.gstatic.com/generate_204`300,,80

custom_proxy_group=🚀 手动选择`select`.*

custom_proxy_group=🇭🇰 香港`url-test`(?i)(香港|港|HK|Hong[ -]?Kong|🇭🇰)`http://www.gstatic.com/generate_204`300,,50

custom_proxy_group=🇨🇳 台湾`url-test`(?i)(台湾|台北|TW|Taiwan|🇨🇳)`http://www.gstatic.com/generate_204`300,,50

custom_proxy_group=🇸🇬 新加坡`url-test`(?i)(新加坡|狮城|坡|SG|Singapore|🇸🇬)`http://www.gstatic.com/generate_204`300,,50

custom_proxy_group=🇯🇵 日本`url-test`(?i)(日本|东京|大阪|JP|Japan|🇯🇵)`http://www.gstatic.com/generate_204`300,,50

custom_proxy_group=🇺🇸 美国`url-test`(?i)(美国|美|US|USA|United States|America|🇺🇸)`http://www.gstatic.com/generate_204`300,,150

custom_proxy_group=🇰🇷 韩国`url-test`(?i)(韩国|首尔|KR|Korea|🇰🇷)`http://www.gstatic.com/generate_204`300,,50

custom_proxy_group=🇬🇧 英国`url-test`(?i)(英国|英格兰|UK|United Kingdom|🇬🇧)`http://www.gstatic.com/generate_204`300,,80

custom_proxy_group=🇩🇪 德国`url-test`(?i)(德国|DE|Germany|🇩🇪)`http://www.gstatic.com/generate_204`300,,80

custom_proxy_group=🇫🇷 法国`url-test`(?i)(法国|FR|France|🇫🇷)`http://www.gstatic.com/generate_204`300,,80

custom_proxy_group=🇦🇺 澳洲`url-test`(?i)(澳洲|澳大利亚|AU|Australia|🇦🇺)`http://www.gstatic.com/generate_204`300,,80

; =========================
; 服务策略组
; =========================

custom_proxy_group=🤖 AI Services`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🇭🇰 香港`[]🇨🇳 台湾`[]🚀 节点选择`[]♻️ 自动选择`[]DIRECT

custom_proxy_group=ChatGPT`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🚀 节点选择`[]DIRECT

custom_proxy_group=Gemini`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🇭🇰 香港`[]🚀 节点选择`[]DIRECT

custom_proxy_group=Telegram`select`[]🇸🇬 新加坡`[]🇺🇸 美国`[]🇭🇰 香港`[]🇨🇳 台湾`[]🇯🇵 日本`[]🚀 节点选择`[]♻️ 自动选择`[]DIRECT

custom_proxy_group=Twitter`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🇬🇧 英国`[]🇭🇰 香港`[]🚀 节点选择`[]DIRECT

custom_proxy_group=YouTube`select`[]🚀 节点选择`[]♻️ 自动选择`[]🇭🇰 香港`[]🇨🇳 台湾`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🇺🇸 美国`[]DIRECT

custom_proxy_group=Netflix`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🇭🇰 香港`[]🇨🇳 台湾`[]🚀 节点选择`[]♻️ 自动选择`[]DIRECT

custom_proxy_group=TikTok`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🇨🇳 台湾`[]🚀 节点选择`[]DIRECT

custom_proxy_group=🌍 Global Media`select`[]🚀 节点选择`[]♻️ 自动选择`[]🇭🇰 香港`[]🇨🇳 台湾`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🇺🇸 美国`[]DIRECT

custom_proxy_group=🇨🇳 China Media`select`[]DIRECT`[]🇭🇰 香港`[]🇨🇳 台湾`[]🚀 节点选择

custom_proxy_group=🎮 Gaming`select`[]🚀 节点选择`[]🇺🇸 美国`[]🇭🇰 香港`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🇨🇳 台湾`[]DIRECT

custom_proxy_group=🍎 Apple`select`[]DIRECT`[]🇭🇰 香港`[]🇺🇸 美国`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🚀 节点选择

custom_proxy_group=Ⓜ️ Microsoft`select`[]DIRECT`[]🇺🇸 美国`[]🇭🇰 香港`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🚀 节点选择

custom_proxy_group=🔎 Google`select`[]🚀 节点选择`[]🇺🇸 美国`[]🇭🇰 香港`[]🇸🇬 新加坡`[]🇯🇵 日本`[]DIRECT

custom_proxy_group=⚡ Speedtest`select`[]DIRECT`[]🚀 节点选择`[]♻️ 自动选择

custom_proxy_group=🎵 Spotify`select`[]🇺🇸 美国`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🚀 节点选择`[]DIRECT

custom_proxy_group=🦋 Bluesky`select`[]🇺🇸 美国`[]🇯🇵 日本`[]🇸🇬 新加坡`[]🚀 节点选择`[]DIRECT

custom_proxy_group=🛑 AdBlock`select`[]REJECT`[]DIRECT

custom_proxy_group=🎯 全球直连`select`[]DIRECT`[]🚀 节点选择

custom_proxy_group=🐟 漏网之鱼`select`[]🚀 节点选择`[]♻️ 自动选择`[]DIRECT`[]🇭🇰 香港`[]🇨🇳 台湾`[]🇸🇬 新加坡`[]🇯🇵 日本`[]🇺🇸 美国`[]🇰🇷 韩国

; =========================
; 基础 / 局域网
; =========================

ruleset=🎯 全球直连,[]GEOIP,LAN
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Lan/Lan.list

; =========================
; 你原配置中的自定义规则
; =========================

ruleset=🎯 全球直连,[]DOMAIN-KEYWORD,115
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/DouYin/DouYin.list
ruleset=🦋 Bluesky,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Bluesky/Bluesky.list

; =========================
; GitHub / Docker
; =========================

ruleset=💻 GitHub,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/GitHub/GitHub.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Developer/Developer.list
ruleset=🚀 节点选择,[]DOMAIN,docker.com
ruleset=🚀 节点选择,[]DOMAIN,docker.io
ruleset=🚀 节点选择,[]DOMAIN,hub.docker.com
ruleset=🚀 节点选择,[]DOMAIN,cloudflare.docker.com

; =========================
; AI
; =========================

ruleset=ChatGPT,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/OpenAI/OpenAI.list
ruleset=🤖 AI Services,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Claude/Claude.list
ruleset=Gemini,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Gemini/Gemini.list
ruleset=🤖 AI Services,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Bing/Bing.list
ruleset=🤖 AI Services,[]DOMAIN-SUFFIX,apple-relay.apple.com
ruleset=🤖 AI Services,[]DOMAIN-SUFFIX,apple-relay.cloudflare.com
ruleset=🤖 AI Services,[]DOMAIN-KEYWORD,apple-relay

; Gemini 补充域名（保留原配置逻辑）
ruleset=Gemini,[]DOMAIN-SUFFIX,googlevideo.com
ruleset=Gemini,[]DOMAIN-SUFFIX,maps.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,speech.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,gstatic.com
ruleset=Gemini,[]DOMAIN-SUFFIX,googleusercontent.com
ruleset=Gemini,[]DOMAIN-SUFFIX,content-autofill.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,clients6.google.com
ruleset=Gemini,[]DOMAIN-SUFFIX,oauth2.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,accounts.google.com
ruleset=Gemini,[]DOMAIN-SUFFIX,proactivebackend-pa.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,generativelanguage.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,alkalimojo-pa.googleapis.com
ruleset=Gemini,[]DOMAIN-SUFFIX,gemini.google.com

; =========================
; Telegram / 社交
; =========================

ruleset=Telegram,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Telegram/Telegram.list
ruleset=Twitter,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Twitter/Twitter.list
ruleset=Twitter,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Threads/Threads.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Facebook/Facebook.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Instagram/Instagram.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Whatsapp/Whatsapp.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Discord/Discord.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/KakaoTalk/KakaoTalk.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Line/Line.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/LinkedIn/LinkedIn.list

; =========================
; 流媒体
; =========================

ruleset=YouTube,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/YouTube/YouTube.list
ruleset=YouTube,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/YouTubeMusic/YouTubeMusic.list
ruleset=Netflix,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Netflix/Netflix.list
ruleset=TikTok,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/TikTok/TikTok.list
ruleset=🌍 Global Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Disney/Disney.list
ruleset=🌍 Global Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Spotify/Spotify.list
ruleset=🌍 Global Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/BBC/BBC.list
ruleset=🌍 Global Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/GlobalMedia/GlobalMedia.list
ruleset=🌍 Global Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Emby/Emby.list

; =========================
; 国内媒体
; =========================

ruleset=🇨🇳 China Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/CCTV/CCTV.list
ruleset=🇨🇳 China Media,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/ChinaMedia/ChinaMedia.list

; =========================
; 游戏
; =========================

ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Game/Game.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Steam/Steam.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/SteamCN/SteamCN.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/PlayStation/PlayStation.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/EA/EA.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Nintendo/Nintendo.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Riot/Riot.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Xbox/Xbox.list
ruleset=🎮 Gaming,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/HoYoverse/HoYoverse.list

; =========================
; Apple
; =========================

ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AppStore/AppStore.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/iCloud/iCloud.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/TestFlight/TestFlight.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AppleMail/AppleMail.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AppleMusic/AppleMusic.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AppleNews/AppleNews.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AppleTV/AppleTV.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Siri/Siri.list
ruleset=🍎 Apple,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Apple/Apple.list
ruleset=🎯 全球直连,[]DOMAIN-SUFFIX,applemusic.com
ruleset=🎯 全球直连,[]DOMAIN-SUFFIX,itunes.apple.com
ruleset=🎯 全球直连,[]DOMAIN-SUFFIX,mzstatic.com

; =========================
; Microsoft / Google
; =========================

ruleset=Ⓜ️ Microsoft,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Microsoft/Microsoft.list
ruleset=Ⓜ️ Microsoft,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Bing/Bing.list
ruleset=🔎 Google,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Google/Google.list
ruleset=🔎 Google,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/GoogleDrive/GoogleDrive.list
ruleset=🔎 Google,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/GoogleSearch/GoogleSearch.list

; =========================
; 其他服务
; =========================

ruleset=⚡ Speedtest,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Speedtest/Speedtest.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Cloudflare/Cloudflare.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Amazon/Amazon.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/PayPal/PayPal.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/LastPass/LastPass.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/TeamViewer/TeamViewer.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Tesla/Tesla.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/PikPak/PikPak.list
ruleset=🚀 节点选择,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Scholar/Scholar.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Download/Download.list

; =========================
; 国内服务
; =========================

ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/WeChat/WeChat.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Zhihu/Zhihu.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/XiaoHongShu/XiaoHongShu.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/China/China.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/ChinaTest/ChinaTest.list
ruleset=🎯 全球直连,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/DNS/DNS.list

; =========================
; 特殊服务
; =========================

ruleset=🚀 节点选择,[]DOMAIN-SUFFIX,api.themoviedb.org
ruleset=🚀 节点选择,[]DOMAIN-SUFFIX,nssurge.com
ruleset=🚀 节点选择,[]DOMAIN-SUFFIX,vercel.app
ruleset=🛑 AdBlock,[]DOMAIN,app-site-association.cdn-apple.com
ruleset=🛑 AdBlock,[]AND,((PROTOCOL,UDP),(DOMAIN-SUFFIX,googlevideo.com))
ruleset=🎯 全球直连,https://raw.githubusercontent.com/zxfccmm4/Profiles/main/Surge/Ruleset/Unbreak.list

; =========================
; 广告 / 隐私
; =========================

ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AdvertisingLite/AdvertisingLite.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Advertising/Advertising.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/AdvertisingTest/AdvertisingTest.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/ZhihuAds/ZhihuAds.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/BlockHttpDNS/BlockHttpDNS.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Hijacking/Hijacking.list
ruleset=🛑 AdBlock,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Privacy/Privacy.list

; =========================
; 中国 IP / 最终规则
; =========================

ruleset=🎯 全球直连,[]GEOIP,CN
ruleset=🐟 漏网之鱼,[]FINAL
