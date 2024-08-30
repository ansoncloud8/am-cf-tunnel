# [am-cf-tunnel](https://github.com/amclubs/am-cf-tunnel)
▶️ **新人[YouTube](https://youtube.com/@AM_CLUB)** 需要您的支持，请务必帮我**点赞**、**关注**、**打开小铃铛**，***十分感谢！！！*** ✅
</br>🎁 不要只是下载或Fork。请 **follow** 我的GitHub、给我所有项目一个 **Star** 星星（拜托了）！你的支持是我不断前进的动力！ 💖
</br>✅**解锁更多技术请访问[【个人博客】](https://am.809098.xyz)**,加入TG群[【AM科技 | 分享交流群】](https://t.me/AM_CLUBS) 
#

# Cloudflare Workers 和 Pages 生成VLESS节点,实现订阅连接可以一键订阅节点

这是一个基于 Cloudflare Workers 和 Pages平台的脚本，在原版的基础上修改了显示 VLESS 配置信息转换为订阅内容。使用该脚本，你可以方便地将 VLESS、trojan 配置信息使用在线配置转换到 Clash、 Singbox 、Quantumult X等工具中。

- VLESS免费节点部署视频教程：[点击进入观看](https://www.youtube.com/watch?v=f9hDJCqAEGA) 
- Trojan免费节点部署视频教程：[点击进入观看](https://youtu.be/1ixc2A9rchM) 
- 优选IP和优选反代IP视频教程：[点击进入观看](https://youtu.be/pKrlfRRB0gU) 
- 聚合节点订阅视频教程：[点击进入观看](https://youtu.be/YBO2hf96150)
- 免费订阅：[进群发关键字: 订阅](https://t.me/AM_CLUBS)

## 订阅工具 [点击进入视频教程](https://youtu.be/xGOL57cmvaw) [点进进入karing视频教程](https://youtu.be/M3vLLBWfuFg)
- [(安卓)v2rayNG](https://github.com/2dust/v2rayNG/releases)      [(安卓)singbox](https://github.com/SagerNet/sing-box/releases)      [(苹果)singbox](https://github.com/SagerNet/sing-box/releases)      [(苹果)Hiddify](https://github.com/hiddify/hiddify-next/releases)
- [(win)v2rayN](https://github.com/2dust/v2rayN/releases)      [(win)singbox](https://github.com/SagerNet/sing-box/releases)      [(win)clashvergerev](https://github.com/clash-verge-rev/clash-verge-rev/releases)      [(win)Hiddify](https://github.com/hiddify/hiddify-next/releases)      [(win)clashnyanpasu](https://github.com/LibNyanpasu/clash-nyanpasu/releases)      [(mac)clashnyanpasu](https://github.com/LibNyanpasu/clash-nyanpasu/releases)
- [(mac)v2rayU](https://github.com/yanue/V2rayU/releases)      [(mac)singbox](https://github.com/SagerNet/sing-box/releases)      [(mac)clashvergerev](https://github.com/clash-verge-rev/clash-verge-rev/releases)      [(mac)Hiddify](https://github.com/hiddify/hiddify-next/releases)

# 免责声明

本免责声明适用于 GitHub 上的 “am-cf-tunnel” 项目（以下简称“该项目”），项目链接为：https://github.com/amclubs/am-cf-tunnel

### 用途
该项目被设计和开发仅供学习、研究和安全测试目的。它旨在为安全研究者、学术界人士和技术爱好者提供一个了解和实践网络通信技术的工具。

### 合法性
使用者在下载和使用该项目时，必须遵守当地法律和规定。使用者有责任确保他们的行为符合其所在地区的法律、规章以及其他适用的规定。

### 免责
1. 作为该项目的作者，我（以下简称“作者”）强调该项目应仅用于合法、道德和教育目的。
2. 作者不鼓励、不支持也不促进任何形式的非法使用该项目。如果发现该项目被用于非法或不道德的活动，作者将强烈谴责这种行为。
3. 作者对任何人或团体使用该项目进行的任何非法活动不承担责任。使用者使用该项目时产生的任何后果由使用者本人承担。
4. 作者不对使用该项目可能引起的任何直接或间接损害负责。
5. 通过使用该项目，使用者表示理解并同意本免责声明的所有条款。如果使用者不同意这些条款，应立即停止使用该项目。

作者保留随时更新本免责声明的权利，且不另行通知。最新的免责声明版本将会在该项目的 GitHub 页面上发布。

## Workers 部署方法 [视频教程](https://www.youtube.com/watch?v=f9hDJCqAEGA)
1. 部署 Cloudflare Worker：
   - 在 Cloudflare Worker 控制台中创建一个新的 Worker。
   - 将 [_worker.js](https://github.com/amclubs/am-cf-tunnel/blob/main/_worker.js) 的内容粘贴到 Worker 编辑器中。
   - 将第 6 行 `userID` 修改成你自己的 **UUID** 。
2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 workers绑定 自定义域： 
   - 在 workers控制台的 `触发器`选项卡，下方点击 `添加自定义域`。
   - 填入你已转入 CloudFlare 域名解析服务的次级域名，例如:`vless.google.com`后 点击`添加自定义域`，等待证书生效即可。

</details>

## Pages 上传 部署方法 **最佳推荐!!!** [视频教程](https://www.youtube.com/watch?v=8oZvklBkMj4)
1. 部署 Cloudflare Pages：
   - 下载 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/_worker.js.zip) 文件，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `上传资产`后，为你的项目取名后点击 `创建项目`，然后上传你下载好的 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/_worker.js.zip) 文件后点击 `部署站点`。
   - 部署完成后点击 `继续处理站点` 后，选择 `设置` > `环境变量` > **制作**为生产环境定义变量 > `添加变量`。
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存`即可。
   - 返回 `部署` 选项卡，在右下角点击 `创建新部署` 后，重新上传 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/_worker.js.zip) 文件后点击 `保存并部署` 即可。
2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 Pages绑定 CNAME自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `google.com`，则添加自定义域填入 `vless.google.com`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `vless`的 CNAME记录 `vless.google.pages.dev` 后，点击 `激活域`即可。

</details>

## Pages GitHub 部署方法 [视频教程](https://youtu.be/6lhFb4hYTYw)
1. 部署 Cloudflare Pages：
   - 在 Github 上先 Fork 本项目，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `连接到 Git`后，选中 `am-tunnel`项目后点击 `开始设置`。
   - 在 `设置构建和部署`页面下方，选择 `环境变量（高级）`后并 `添加变量`
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存并部署`即可。

2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 Pages绑定 CNAME自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `google.com`，则添加自定义域填入 `vless.google.com`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `vless`的 CNAME记录 `vless.google.pages.dev` 后，点击 `激活域`即可。


</details>

## 变量说明
| 变量名 | 示例 | 必填 | 备注 | YT |
|-----|-----|-----|-----|-----|
| UUID | 90cd4a77-141a-43c9-991b-08263cfe9c10 |√| [在线获取UUID](https://1024tools.com/uuid)|  |
| PROXYIP | cdn-b100.xn--b6gac.eu.org |❌| 备选作为访问CloudFlareCDN站点的代理节点(支持多ProxyIP, ProxyIP之间使用`,`或 换行 作间隔) | [Video](https://youtu.be/pKrlfRRB0gU) |
| SOCKS5    | user:password@127.0.0.1:1080  |❌                               | 优先作为访问CFCDN站点的SOCKS5代理                            |[Video](https://youtu.be/Bw82BH_ecC4) |
| ADD | `icook.tw:2053#官方优选域名` |❌| 本地优选TLS域名/优选IP(支持多元素之间`,`或 换行 作间隔) ||
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/ipv4.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) |[Video](https://youtu.be/dzxezRV1v-o) |
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/ipv4.csv) |❌| iptest测速结果(支持多元素, 元素之间使用`,`作间隔) |[Video](https://youtu.be/vX3U3FuuTT8)|
| ADDNOTLS | `icook.hk:8080#官方优选域名` |❌| 本地优选noTLS域名/优选IP(支持多元素之间`,`或 换行 作间隔) ||
| ADDNOTLSAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/amclubs/am-cf-tunnel/main/ipv4.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| SUB       | trojan.cftest.dynv6.net   |❌                                       | 优选订阅生成器地址(使用订阅器将放弃`ADD`内的本地优选订阅内容) ||
| SUBAPI    | subapi.cftest.dynv6.net  |❌                                    | clash、singbox等 订阅转换后端                                ||
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_Mini.ini](https://raw.githubusercontent.com/amclubs/ACL4SSR/main/Clash/config/ACL4SSR_Online_Full_MultiMode.ini) |❌  | clash、singbox等 订阅转换配置文件  ||
| SUBNAME   | am-cf-tunnel  |❌                                                      | 订阅名称                                                     ||
| DLS | `8` |❌| `ADDCSV`测速结果满足速度下限 ||
| DLS       | 8        |❌                                                     | `ADDCSV`测速结果满足速度下限                                 ||
| TGTOKEN   | 6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXXXXqWXgBA     |❌           | 发送TG通知的机器人token                                      ||
| TGID      | 6946912345    |❌                                                | 接收TG通知的账户数字ID                                       ||
| RPROXYIP  | false       |❌                                                  | 设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)      ||
| URL302    | https://t.me/AM_CLUBS       |❌                              | 主页302跳转(支持多url, url之间使用`,`或 换行 作间隔, 小白别用) ||
| URL       | https://t.me/AM_CLUBS   |❌                                  | 主页伪装(支持多url, url之间使用`,`或 换行 作间隔, 乱设容易触发反诈) ||
| CFEMAIL   | test@gmail.com         |❌                                      | CF账户邮箱(与`CFKEY`都填上后, 订阅信息将显示请求使用量, 小白别用) ||
| CFKEY     | c6a944b5c956b6c18c2352880952bced8b85e     |❌                    | CF账户Global API Key(与`CFEMAIL`都填上后, 订阅信息将显示请求使用量, 小白别用) ||


## 已适配自适应订阅内容
   - [v2rayN](https://github.com/2dust/v2rayN)
   - [v2rayU](https://github.com/yanue/V2rayU/releases)
   - [sing-box](https://github.com/SagerNet/sing-box)
   - clash.meta（[clash-verge-rev
](https://github.com/clash-verge-rev/clash-verge-rev)，[Clash Nyanpasu](https://github.com/keiko233/clash-nyanpasu)，~[clash-verge](https://github.com/zzzgydi/clash-verge/tree/main)~，ClashX Meta、openclash）
   - Quantumult X
   - 小火箭
   - surge

# 感谢
[3Kmfi6HP](https://github.com/3Kmfi6HP/EDtunnel)、[ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master/Clash/config)

 # 
<center><details><summary><strong> [点击展开] 赞赏支持 ~🧧</strong></summary>
*我非常感谢您的赞赏和支持，它们将极大地激励我继续创新，持续产生有价值的工作。*
  
- **USDT-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`
  
</details></center>
