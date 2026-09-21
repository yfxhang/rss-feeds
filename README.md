# 本机 RSS 源镜像

由本机（changan）定时生成后推送到此仓库，供「开悟」等平台抓取。每次推送为覆盖式更新。

最近一次推送：2026-09-21 09:15:25

## 读取地址（三种任选，平台侧哪个能访问用哪个）

1. raw.githubusercontent.com（GitHub 官方，国内可能被墙）：
   `https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`
2. jsDelivr CDN（国内一般可访问，有缓存延迟）：
   `https://cdn.jsdelivr.net/gh/yfxhang/rss-feeds@main/<文件路径>`
3. ghproxy 前缀代理：
   `https://ghproxy.net/https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`

## 源清单

| 源 | 仓库内路径 | 条数 | 本机生成时间 |
|---|---|---|---|
| 工信部·工信动态（清洗源） | `rss/miit.xml` | 60 | 2026-09-20 18:21:23 |
| 中国能源网（自建 CSS 路由） | `rss/china5e.xml` | 254 | 2026-09-20 18:22:29 |
| 标签聚合·矿产 | `rss/tag/kuangchan.xml` | 6 | 2026-09-20 18:25:01 |
| 标签聚合·材料 | `rss/tag/cailiao.xml` | 21 | 2026-09-20 18:25:01 |
| 标签聚合·电芯 | `rss/tag/dianxin.xml` | 24 | 2026-09-20 18:25:01 |
| 标签聚合·电池回收 | `rss/tag/dianchihuishou.xml` | 4 | 2026-09-20 18:25:01 |
| 标签聚合·新能源汽车 | `rss/tag/xinnengyuan.xml` | 1 | 2026-09-20 18:25:01 |
| 标签聚合·政策法规 | `rss/tag/zhengce.xml` | 6 | 2026-09-20 18:25:01 |

## 说明

- 工信部源为清洗版：源站原始 feed 是 13 位毫秒时间戳、2.1 万条、按栏目分块乱序，这里已转标准时间并按时间倒序裁到最近 60 条。
- 标签聚合源的关键词来自 `input.xlsx` 派生表，窗口 48 小时，每标签最多 60 条。
- 机器不在线时不会推送，仓库里保留的是最后一次成功推送的内容（`index.json` 里有生成时间，可据此判断新鲜度）。
- 机器可读的清单见 `index.json`。