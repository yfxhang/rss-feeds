# 本机 / 云端 RSS 源镜像

由 GitHub Actions 定时抓取生成后推送到此仓库（2026-09-29 起由云端生成，不再依赖本机开机），供「开悟」等平台抓取。每次推送为覆盖式更新。

最近一次推送：2026-10-10 15:01:52（北京时间）

## 读取地址（平台侧哪个能访问用哪个）

1. ghproxy 前缀代理（平台当前主用，最实时）：
   `https://ghproxy.net/https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`
2. fastly jsDelivr CDN（有缓存延迟）：
   `https://fastly.jsdelivr.net/gh/yfxhang/rss-feeds@main/<文件路径>`
3. GitHub 官方 raw（国内常被墙）：
   `https://raw.githubusercontent.com/yfxhang/rss-feeds/main/<文件路径>`

机器可读清单：`index.json`（含每个源的条数与生成时间，可用于判断新鲜度）。

## 源清单

| 源 | 仓库内路径 | 条数 | 本轮生成时间（北京） |
|---|---|---|---|
| 工信部·工信动态（清洗源） | `rss/miit.xml` | 60 | 2026-10-10 14:58:33 |
| 中国能源网（自建 CSS 路由） | `rss/china5e.xml` | 260 | 2026-10-10 15:00:32 |
| 标签聚合·矿产 | `rss/tag/kuangchan.xml` | 4 | 2026-10-10 15:01:51 |
| 标签聚合·材料 | `rss/tag/cailiao.xml` | 25 | 2026-10-10 15:01:51 |
| 标签聚合·电芯 | `rss/tag/dianxin.xml` | 24 | 2026-10-10 15:01:51 |
| 标签聚合·电池回收 | `rss/tag/dianchihuishou.xml` | 5 | 2026-10-10 15:01:51 |
| 标签聚合·新能源汽车 | `rss/tag/xinnengyuan.xml` | 2 | 2026-10-10 15:01:51 |
| 标签聚合·政策法规 | `rss/tag/zhengce.xml` | 15 | 2026-10-10 15:01:51 |
| 全国标准信息公共服务平台·国家标准动态 | `rss/site/samr_gb.xml` | 30 | 2026-10-10 15:00:37 |
| 全国汽车标准化委员会·标准计划公告 | `rss/site/catarc_plan.xml` | 30 | 2026-10-10 15:00:35 |
| 全国汽车标准化委员会·公开征求意见 | `rss/site/catarc_opinion.xml` | 30 | 2026-10-10 15:00:36 |
| 全国汽车标准化委员会·标准发布公告 | `rss/site/catarc_release.xml` | 30 | 2026-10-10 15:00:35 |
| 上海金属网·快讯 | `rss/site/shmet_flash.xml` | 400 | 2026-10-10 15:01:24 |
| 上海金属网·快讯A（新） | `rss/site/shmet_flash_a.xml` | 176 | 2026-10-10 15:01:23 |
| 上海金属网·快讯B（中） | `rss/site/shmet_flash_b.xml` | 176 | 2026-10-10 15:01:25 |
| 上海金属网·快讯C（旧） | `rss/site/shmet_flash_c.xml` | 178 | 2026-10-10 15:01:29 |
| 盖世汽车·最新资讯 | `rss/site/gasgoo.xml` | 18 | 2026-10-10 15:00:38 |
| 佐思汽研·研究报告与资讯 | `rss/site/shujubang.xml` | 6 | 2026-10-10 15:00:36 |
| 国家标准化管理委员会·标准化要闻 | `rss/site/sac_bzhyw.xml` | 20 | 2026-10-10 15:00:38 |
| CEN/CENELEC·新闻 | `rss/site/cencenelec.xml` | 10 | 2026-10-10 15:00:46 |
| 中国有色网·重点新闻 | `rss/site/cnmn_news.xml` | 20 | 2026-10-10 15:00:39 |
| 中国有色网·政策法规 | `rss/site/cnmn_policy.xml` | 20 | 2026-10-10 15:00:40 |
| 中国汽车动力电池产业创新联盟·动态 | `rss/site/caev.xml` | 15 | 2026-10-10 15:00:49 |
| 乘用车市场信息联席会·行业新闻 | `rss/site/cpcaauto.xml` | 20 | 2026-10-10 15:00:51 |
| 电池中国·行业资讯 | `rss/site/ciaps.xml` | 20 | 2026-10-10 15:01:08 |
| 电池中国·协会动态 | `rss/site/ciaps_hy.xml` | 19 | 2026-10-10 15:01:13 |
| 中汽协·首页要闻 | `rss/site/caam.xml` | 30 | 2026-10-10 15:01:00 |
| 中汽研·汽车标准化新闻 | `rss/site/catarc_news.xml` | 20 | 2026-10-10 15:00:53 |
| 工信部·节能与综合利用司 | `rss/site/miit_jns.xml` | 30 | 2026-10-10 15:01:02 |
| 维科网·智能汽车 | `rss/site/ofweek.xml` | 600 | 2026-10-10 15:01:51 |
| 艾邦锂电网·资讯 | `rss/site/aibanglib.xml` | 15 | 2026-10-10 15:01:10 |

## 平台可直接订阅的原生源（不经本仓库）

| 源 | URL |
|---|---|
| ITU（国际电信联盟）新闻 | https://www.itu.int/hub/feed/ |
| IEEE Spectrum 新闻 | https://spectrum.ieee.org/feeds/feed.rss |
| IEEE Spectrum 能源专题 | https://spectrum.ieee.org/feeds/topic/energy.rss |

## 说明

- 生成器代码在仓库 `feeds/`：`site_feeds.py`（无 RSS 站点自建源）、`miit_news.py`（工信部清洗）、`lib/china5e_rss.py`（中国能源网 CSS 路由）、`build_tags.py`（标签聚合）。
- 某个源某轮抓不到时**保留上一版**，不会被空文件覆盖。
- 中文文件名（标签、站点）在仓库内使用拼音/英文 slug，映射见 `feeds/stage_publish.py`。