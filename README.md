# 本机 RSS 源镜像

由本机（changan）定时生成后推送到此仓库，供「开悟」等平台抓取。每次推送为覆盖式更新。

最近一次推送：2026-09-21 10:06:22

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
| 工信部·工信动态（清洗源） | `rss/miit.xml` | 60 | 2026-09-21 10:04:28 |
| 中国能源网（自建 CSS 路由） | `rss/china5e.xml` | 259 | 2026-09-21 10:05:06 |
| 标签聚合·矿产 | `rss/tag/kuangchan.xml` | 7 | 2026-09-21 10:05:06 |
| 标签聚合·材料 | `rss/tag/cailiao.xml` | 25 | 2026-09-21 10:05:06 |
| 标签聚合·电芯 | `rss/tag/dianxin.xml` | 25 | 2026-09-21 10:05:06 |
| 标签聚合·电池回收 | `rss/tag/dianchihuishou.xml` | 5 | 2026-09-21 10:05:06 |
| 标签聚合·新能源汽车 | `rss/tag/xinnengyuan.xml` | 2 | 2026-09-21 10:05:06 |
| 标签聚合·政策法规 | `rss/tag/zhengce.xml` | 8 | 2026-09-21 10:05:06 |
| 全国标准信息公共服务平台·国家标准动态 | `rss/site/samr_gb.xml` | 30 | 2026-09-21 10:05:07 |
| 全国汽车标准化委员会·标准计划公告 | `rss/site/catarc_plan.xml` | 30 | 2026-09-21 10:05:08 |
| 全国汽车标准化委员会·公开征求意见 | `rss/site/catarc_opinion.xml` | 30 | 2026-09-21 10:05:09 |
| 全国汽车标准化委员会·标准发布公告 | `rss/site/catarc_release.xml` | 30 | 2026-09-21 10:05:10 |
| 上海金属网·快讯 | `rss/site/shmet_flash.xml` | 120 | 2026-09-21 10:05:16 |
| CEN/CENELEC·新闻 | `rss/site/cencenelec.xml` | 10 | 2026-09-21 10:03:37 |
| 中国有色网·重点新闻 | `rss/site/cnmn_news.xml` | 20 | 2026-09-21 10:03:37 |
| 中国有色网·政策法规 | `rss/site/cnmn_policy.xml` | 20 | 2026-09-21 10:03:38 |
| 中国汽车动力电池产业创新联盟·动态 | `rss/site/caev.xml` | 15 | 2026-09-21 10:03:38 |
| 乘用车市场信息联席会·行业新闻 | `rss/site/cpcaauto.xml` | 20 | 2026-09-21 10:03:42 |
| 电池中国·行业资讯 | `rss/site/ciaps.xml` | 20 | 2026-09-21 10:03:43 |
| 电池网·首页要闻 | `rss/site/cbea.xml` | 30 | 2026-09-21 10:03:43 |
| 维科网·智能汽车 | `rss/site/ofweek.xml` | 20 | 2026-09-21 10:03:44 |
| 艾邦锂电网·资讯 | `rss/site/aibanglib.xml` | 10 | 2026-09-21 10:03:45 |

## 平台可直接订阅的原生源（不经本机）

| 源 | URL |
|---|---|
| ITU（国际电信联盟）新闻 | https://www.itu.int/hub/feed/ |
| IEEE Spectrum 新闻 | https://spectrum.ieee.org/feeds/feed.rss |
| IEEE Spectrum 能源专题 | https://spectrum.ieee.org/feeds/topic/energy.rss |
## 读取地址（按本机实测可用性排序，平台侧哪个能访问用哪个）

1. **fastly.jsdelivr CDN（本机实测通，推荐）**：
   `https://fastly.jsdelivr.net/gh/yfxhang/rss-feeds@main/<文件路径>`
2. **ghproxy 前缀代理（本机实测通）**：
   `https://ghproxy.net/https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`
3. cdn.jsdelivr CDN（备用，本机时通时断）：
   `https://cdn.jsdelivr.net/gh/yfxhang/rss-feeds@main/<文件路径>`
4. GitHub 官方 raw（国内常被墙，平台侧若能访问则最实时）：
   `https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`

机器可读清单：`index.json`（含每个源的条数与生成时间，可用于判断新鲜度）。

## 说明


- 工信部源为清洗版：源站原始 feed 是 13 位毫秒时间戳、2.1 万条、按栏目分块乱序，这里已转标准时间并按时间倒序裁到最近 60 条。
- `rss/site/*.xml` 是「无公开 RSS 站点」的自建源（来源：无RSS源站点订阅方案调研_2026-09-20.pdf 的 A/B/C 档），抓取器在本机 `C:\HERMES\feedservice\site_feeds.py`。
- 列表页没有发布时间的源（电池网）不写 `pubDate`，由阅读器按抓取时间入库；上海金属网快讯为高频道（全天 400+ 条），按 6 小时分段采样、每次最多 120 条。
- 标签聚合源的关键词来自 `input.xlsx` 派生表，窗口 48 小时，每标签最多 60 条。
- 机器不在线时不会推送，仓库里保留的是最后一次成功推送的内容（`index.json` 里有生成时间，可据此判断新鲜度）。
- 机器可读的清单见 `index.json`。