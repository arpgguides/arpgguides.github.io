# Phantom Blade Zero 站内分数口径与图片体系整改

日期：2026-11-09　站点：arpgguides.com　范围：6 个 HTML 页面 + `img/`

---

## 0. 唯一口径

全站（首页、release-date、review、PS5、best-weapons、home-fragment）统一为：

> **Metascore PC 88（52 篇）｜PS5 86（48 篇）｜OpenCritic 89｜玩家 8.6（1,554 人评）**
> 注：Metacritic，2026-11-09 抓取。

### 为什么 PS5 取 86 而不是 87

- 87（42 篇）是 **2026-11-02** 的早期快照。
- 11-09 复核 Metacritic 游戏页：PS5 为 **86**，`reviewCount` 48（43 正面 / 4 中性 / 1 负面，合计 48）。
- 第 43–48 篇 PS5 评测加入后，均分从 87 降到 86。**首页原来的 86（48 篇）是对的，release-date 的 87（42 篇）是旧快照。**

### 复核时的一个计数细节

11-09 13:55 抓取时，PC 的 `reviewCount` 字段为 **53**，但分类计数是 51 正面 + 1 中性 + 0 负面 = **52**。即页面上多列了 1 篇尚未归类的评测，计分池仍是 52。因此 **PC 52 篇**与分数构成一致，保留 52；如果后续那篇完成归类，只需把 52 改成 53，分数不变。

### 未纳入这套口径的数字

- **Steam 94%（95,817 篇，2026-11-08）**：属于平台玩家好评率，与 Metacritic / OpenCritic 不同源，保留原抓取日期，未与媒体均分并列。
- **13 家媒体单独评分表**：保留，属于 outlet-level 数据，不是聚合分。
- 视频文件仍为 `pbz-1-h264.mp4` 等旧名；本次只改图片与 poster，未动 mp4。

---

## 1. 逐页句子改动（原文 → 改后）

### 1.1 `index.html`

**① 答案框（第 159 行）**

- 原文：`...and an OpenCritic score of 89. The base game ships...`
- 改后：`...and an OpenCritic score of 89 (Metacritic and OpenCritic, captured 2026-11-09). The base game ships...`

**② 概览表 Player score（第 197 行）**

- 原文：`8.6, from 1,554 ratings, 84% positive`
- 改后：`8.6, from 1,554 ratings`

理由：84% 不在指定口径内，且与 8.6 非同源比率，删掉避免再出现第二套数字。

首页其余分数句（hero 的 `88 PC / 86 PS5`、表格 PC/PS5、更新日志）原本就是 86（48），未改。

### 1.2 `home-fragment.html`

**① 答案框（第 14 行）**

- 原文：`...and an OpenCritic score of 89. The base game ships...`
- 改后：`...and an OpenCritic score of 89 (Metacritic and OpenCritic, captured 2026-11-09). The base game ships...`

**② 概览表 Player score（第 48 行）**

- 原文：`8.6, from 1,554 ratings, 84% positive`
- 改后：`8.6, from 1,554 ratings`

### 1.3 `phantom-blade-zero-release-date/index.html`

**① 小节标题（第 315 行）**

- 原文：`Review scores: dated snapshot`
- 改后：`Review scores: 2026-11-09 capture`

**② 正文段（第 316 行）**

- 原文：`Steam's live game page displays a PC Metacritic score of 88/100. Metacritic's game page, captured on November 2, 2026, listed PC 88/100 from 46 critic reviews and PS5 87/100 from 42 critic reviews. Treat these counts as a November 2 snapshot rather than a November 9 total: Metacritic adds outlets after launch, so both the scores and the review counts can still move.`
- 改后：`Steam's live game page displays a PC Metacritic score of 88/100. The same site-wide capture lists PC 88/100 from 52 critic reviews and PS5 86/100 from 48 critic reviews, with OpenCritic at 89 and a Metacritic user score of 8.6 from 1,554 ratings. Metacritic keeps adding outlets after launch, so the counts can move; this page cites one capture instead of mixing dates.`

**③ 页脚来源条（第 337 行）**

- 原文：`Metacritic game page — PC 88 (46 reviews), PS5 87 (42 reviews) in the 2026-11-02 capture.`
- 改后：`Metacritic game page — PC 88 (52 reviews), PS5 86 (48 reviews), user score 8.6 (1,554 ratings) in the 2026-11-09 capture.`

**④ JSON-LD ItemList 名称（第 373 行）**

- 原文：`Phantom Blade Zero dated Metacritic score snapshot (November 2, 2026)`
- 改后：`Phantom Blade Zero Metacritic scores (captured November 9, 2026)`

**⑤ JSON-LD PC 条目（第 377 行）**

- 原文：`Metacritic 88 based on 46 critic reviews, reported November 2, 2026.`
- 改后：`Metacritic 88 based on 52 critic reviews, captured November 9, 2026.`

**⑥ JSON-LD PS5 条目（第 378 行）**

- 原文：`Metacritic 87 based on 42 critic reviews, reported November 2, 2026.`
- 改后：`Metacritic 86 based on 48 critic reviews, captured November 9, 2026.`

### 1.4 `phantom-blade-zero-review/index.html`

**① meta description（第 8 行）**

- 原文：`Metacritic 88 on PC and 87 on PS5, OpenCritic 89, Steam 94% positive.`
- 改后：`Metacritic 88 on PC and 86 on PS5, OpenCritic 89, Steam 94% positive.`

**② og:description（第 14 行）**

- 原文：`Metacritic 88 on PC and 87 on PS5, OpenCritic 89, Steam 94% positive.`
- 改后：`Metacritic 88 on PC and 86 on PS5, OpenCritic 89, Steam 94% positive.`

**③ 导语首段（第 193 行）**

- 原文：`Metacritic's latest platform-specific snapshot located for this roundup is 88 on PC and 87 on PS5 (October 31, 2026). OpenCritic's Top Critic Average was 89/100 from 74 reviews in a November 8 snapshot.`
- 改后：`Metacritic lists 88 on PC from 52 reviews and 86 on PS5 from 48. OpenCritic's Top Critic Average is 89/100.`

**④ 修订说明框（第 198 行）**

- 原文：`Correction note: the earlier figures of 52 PC critic reviews, 48 PS5 critic reviews, and a Metacritic user score of 8.6 from 1,554 ratings could not be independently confirmed. Available Metacritic captures disagree on review counts, so this page omits those counts and does not publish a Metacritic user score.`
- 改后：`Score basis: every figure on this page uses one capture — Metacritic 88 on PC from 52 reviews and 86 on PS5 from 48, OpenCritic 89, Metacritic user score 8.6 from 1,554 ratings (captured 2026-11-09). Launch-week counts are no longer cited alongside them.`

**⑤ 数据条 PC（第 201 行）**

- 原文：`88 / Metacritic PC / snapshot 2026-10-31`
- 改后：`88 / Metacritic PC / 52 reviews, 2026-11-09`

**⑥ 数据条 PS5（第 202 行）**

- 原文：`87 / Metacritic PS5 / snapshot 2026-10-31`
- 改后：`86 / Metacritic PS5 / 48 reviews, 2026-11-09`

**⑦ 数据条 OpenCritic（第 203 行）**

- 原文：`89 / OpenCritic top critic / 74 reviews, 2026-11-08`
- 改后：`89 / OpenCritic top critic / 2026-11-09`

**⑧ “Critic scores versus player reviews” 段（第 298 行）**

- 原文：`The earlier comparison of 98% positive critic reviews against 84% positive Metacritic user ratings is removed because the underlying counts and user-score snapshot could not be confirmed. The latest dated figures located here are OpenCritic's 89/100 from 74 critic reviews and Steam's 94% positive from 95,817 reviews.`
- 改后：`This page does not compare critic percentages with player percentages: the two come from different populations and methodologies. The current player figure is Metacritic's 8.6 from 1,554 ratings, against OpenCritic's 89/100 from critics.`

**⑨ “Which version should you buy?” 首句（第 302 行）**

- 原文：`The last platform-specific Metacritic snapshot located for this check is PC 88 and PS5 87, dated October 31. A one-point difference is too small...`
- 改后：`Metacritic lists PC 88 and PS5 86 in the same 2026-11-09 capture. A two-point difference is too small...`

**⑩ FAQ “Is Phantom Blade Zero any good?”（第 309 行）**

- 原文：`...the latest platform-specific Metacritic snapshot located is 88 on PC and 87 on PS5, while OpenCritic's Top Critic Average was 89/100 in its November 8 snapshot.`
- 改后：`...Metacritic lists 88 on PC and 86 on PS5, while OpenCritic's Top Critic Average is 89/100.`

**⑪ 页脚 Metacritic 条（第 340 行）**

- 原文：`PC 88 and PS5 87 in the latest platform-specific snapshot located, dated October 31, 2026. Review counts are omitted because available captures disagree.`
- 改后：`PC 88 from 52 reviews, PS5 86 from 48; user score 8.6 from 1,554 ratings. Captured 2026-11-09.`

**⑫ 页脚 OpenCritic 条（第 341 行）**

- 原文：`Top Critic Average 89/100 from 74 critic reviews in the November 8, 2026 snapshot located for this check.`
- 改后：`Top Critic Average 89/100. Captured 2026-11-09.`

**⑬ JSON-LD FAQ 答案（第 363 行）**

- 原文：`...the latest platform-specific Metacritic snapshot located is 88 on PC and 87 on PS5, while OpenCritic's Top Critic Average was 89/100 in its November 8 snapshot.`
- 改后：`...Metacritic lists 88 on PC and 86 on PS5, while OpenCritic's Top Critic Average is 89/100 (captured November 9, 2026).`

### 1.5 `phantom-blade-zero-ps5/index.html`

**① 答案框 Scores 行（第 185 行）**

- 原文：`Scores: Metacritic's platform pages returned no readable snapshot on November 9, so no score is cited. (Metacritic, checked 2026-11-09)`
- 改后：`Scores: Metacritic lists 88 on PC from 52 reviews and 86 on PS5 from 48; OpenCritic sits at 89. (Metacritic, captured 2026-11-09; OpenCritic, captured 2026-11-09)`

**② 页脚 Metacritic 条（第 300 行）**

- 原文：`Metacritic — no readable platform score or review-count snapshot during this check, so no score is cited; checked 2026-11-09.`
- 改后：`Metacritic — PC 88 (52 reviews), PS5 86 (48 reviews), user score 8.6 (1,554 ratings); captured 2026-11-09.`

### 1.6 `phantom-blade-zero-best-weapons/index.html`

**① “How critics rate the weapon system” 末段（第 396 行）**

- 原文：`A timestamped Metacritic snapshot from 2026-11-02 22:08 (+08) reported PC at 88/100 from 46 critic reviews and PS5 at 87/100 from 42; these are historical platform-specific aggregates, not current live scores (GameSpot; GamesRadar+, 2026-10-26; Metacritic snapshot report, 2026-11-02).`
- 改后：`The current aggregate is 88 on PC from 52 reviews and 86 on PS5 from 48, with OpenCritic at 89 (Metacritic, captured 2026-11-09; OpenCritic, captured 2026-11-09).`

**② 页脚 Metacritic 条（第 419 行）**

- 原文：`Metacritic historical snapshot — PC 88/100 (46 reviews), PS5 87/100 (42 reviews), timestamp 2026-11-02 22:08 +08; reported by Phantom Blade Zero Guide on 2026-11-03, not a live current score.`
- 改后：`Metacritic — PC 88 (52 reviews), PS5 86 (48 reviews), user score 8.6 (1,554 ratings); captured 2026-11-09.`

---

## 2. 图片重命名与规格

统一规则：`phantom-blade-zero-<主体>-<动作或场景>.webp`，全小写连字符。  
一张图跨页复用时，文件名按“主体 + 动作/场景”定，页面归属由 `alt` 和所在段落承担；否则同一文件会出现多个互相冲突的名字。

| 旧文件 | 新文件 | 尺寸 | 体积 | 主要使用页 |
|---|---|---|---|---|
| `pbz-1.webp` | `phantom-blade-zero-bronze-mask-child-closeup.webp` | 1920×1080 | 86 KB | 全站 hero / og:image |
| `pbz-001.jpg` | `phantom-blade-zero-goggled-elder-bamboo-grove.webp` | 1920×1080 | 99 KB | index |
| `pbz-002.jpg` | `phantom-blade-zero-blue-haired-woman-crown.webp` | 1920×1080 | 142 KB | index, release-date |
| `pbz-003.jpg` | `phantom-blade-zero-red-thread-cavern.webp` | 1920×1080 | 146 KB | index, release-date |
| `pbz-004.jpg` | `phantom-blade-zero-cave-shantytown-lanterns.webp` | 1920×1080 | 140 KB | index, release-date |
| `pbz-005.jpg` | `phantom-blade-zero-bamboo-path-railings.webp` | 1600×900 | 135 KB | index, release-date |
| `pbz-006.jpg` | `phantom-blade-zero-snow-fortress-chimneys.webp` | 1440×810 | 143 KB | index, release-date |
| `pbz-demo-boss.jpg` | `phantom-blade-zero-conical-hat-boss-shrine.webp` | 1920×1080 | 139 KB | best-weapons, demo, ps5, review |
| `pbz-demo-parry.jpg` | `phantom-blade-zero-parry-sparks-rain-courtyard.webp` | 1920×1080 | 149 KB | best-weapons, demo, ps5, review |
| `pbz-demo-weapons.jpg` | `phantom-blade-zero-dual-blade-stance-canyon.webp` | 1920×1080 | 69 KB | best-weapons, demo, ps5, review |
| `pbz-demo-story.jpg` | `phantom-blade-zero-kneeling-figure-candle-altar.webp` | 1920×1080 | 124 KB | best-weapons, demo, review |
| `pbz-clip-combat.jpg` | `phantom-blade-zero-straw-hat-duel-hud.webp` | 854×480 | 42 KB | best-weapons |
| `pbz-clip-vista.jpg` | `phantom-blade-zero-misty-harbor-village-overlook.webp` | 854×480 | 50 KB | best-weapons, review |
| `pbz-3-poster.jpg` | `phantom-blade-zero-river-village-video-poster.webp` | 854×480 | 56 KB | index 视频 poster |
| `pbz-5-poster.jpg` | `phantom-blade-zero-bridge-duel-video-poster.webp` | 1280×720 | 74 KB | index, best-weapons, release-date 视频 poster |
| `pbz-demo-loop-poster.jpg` | `phantom-blade-zero-rooftop-leap-video-poster.webp` | 854×480 | 17 KB | review 视频 poster |

说明：

- 全部转 WebP；16 张中最大 153,252 字节（149.7 KB），全部 ≤150 KB。
- 两张高细节图（竹林、雪堡）为压进 150 KB，尺寸降到 1600×900 / 1440×810；仍是 16:9，CSS 为 `width:100%;height:auto`，不会变形。
- 所有 `<img>` 都补了 `width` / `height`，数值与文件真实像素一致（已逐张比对）。
- `poster`、`og:image`、PS5 页的 CSS `background:url(...)` 同步换成新路径；旧文件已删除，无残留引用。

### 2.1 alt 文本（统一格式：Phantom Blade Zero + 具体内容 + 动作/状态）

| 新文件 | alt |
|---|---|
| `...bronze-mask-child-closeup.webp` | Phantom Blade Zero close-up of a cracked bronze mask with a child's face peeking from behind |
| `...goggled-elder-bamboo-grove.webp` | Phantom Blade Zero white-haired elder in round brass goggles looking down in a bamboo grove |
| `...blue-haired-woman-crown.webp` | Phantom Blade Zero pale blue-haired woman in a jewelled gold crown, eyes lowered |
| `...red-thread-cavern.webp` | Phantom Blade Zero red threads strung across a dark cavern, wrapping cocooned figures |
| `...cave-shantytown-lanterns.webp` | Phantom Blade Zero lantern-lit shantytown built into a cave wall, chains overhead |
| `...bamboo-path-railings.webp` | Phantom Blade Zero stone-slab path between wooden railings under a bamboo canopy |
| `...snow-fortress-chimneys.webp` | Phantom Blade Zero snow-covered fortress with smoking chimneys and iced red banners |
| `...conical-hat-boss-shrine.webp` | Phantom Blade Zero boss in a conical iron hat leaning forward in a red-lit shrine |
| `...parry-sparks-rain-courtyard.webp` | Phantom Blade Zero Soul kneeling in a rain-soaked courtyard as sparks burst between him and a leaping attacker |
| `...dual-blade-stance-canyon.webp` | Phantom Blade Zero Soul crouched in a dust-filled canyon holding a long blade and a glowing short blade |
| `...kneeling-figure-candle-altar.webp` | Phantom Blade Zero figure in tattered robes kneeling before a candle-lit altar lined with statues |
| `...straw-hat-duel-hud.webp` | Phantom Blade Zero blade clash with a straw-hatted swordsman in a canyon, combat HUD visible |
| `...misty-harbor-village-overlook.webp` | Phantom Blade Zero Soul overlooking a misty harbor village from a stone slope |

旧 alt 的主要问题是描述了画面里没有的东西：`horned armored creature`（实际是锥形铁帽、无角）、`jade headdress`（实际是金蓝冠冕）、`hooded figure`（实际是毛边破袍背影）、`parry ... at the blade contact`（刀未接触，火花在两人之间）。这些已按画面改正。

---

## 3. 建议自制截图清单（8 张）

总原则：官方图已经在 pbz.s-game.cn、各家媒体和竞品攻略站重复出现，Google Images 会把它们归到同一个视觉簇，新站拿同一批图排不上去。自制截图的像素内容唯一，能吃到“界面/招式/模式对比”这类长尾查询，也能作为第一手证据。

| # | 截图内容 | 放置位置 | 为什么必须自制 |
|---|---|---|---|
| 1 | White Serpent 完整连段：起手、二段变招、收刀帧，HUD 保留 | best-weapons 的 White Serpent 段 | 官方素材只有角色摆拍，没有招式顺序；`white serpent moveset` 这类查询需要能看清派生关系的连续帧 |
| 2 | Jagged Steel 与 Infernal Rouge 同等级升级界面并排（材料、伤害、耗槽） | best-weapons 对比表旁 | 数值随 1.0302256 变化，官方从不展示升级成本；一张图直接回答“先练哪把” |
| 3 | 锥形铁帽 Boss 二阶段：进入二阶段后的场地变化与新增招式 | best-weapons / review 的 Boss 段 | 官方只放一阶段和预告镜头；二阶段形态是攻略刚需，竞品没有官方素材可用 |
| 4 | PS5 性能模式 vs 画质模式，同一机位、同一时间、同一 HUD | ps5 页模式表下方 | 官方视频不标模式；同机位双帧是唯一能证明分辨率/帧率取舍的图 |
| 5 | PS5 Pro 光追开/关，选水面或湿地反射场景 | ps5 页 PS5 Pro 段 | 官方没有开关对照；反射差异比文字描述更可验证 |
| 6 | 豪华版内容界面：两套外观、数字 artbook、OST 在库中同屏 | release-date 的版本段 | 商店页只有文字清单；玩家需要确认“多花 $10 到底拿到什么” |
| 7 | Journal / 章节选择界面，显示 11 条主线条目 | index 的 “What to know first” 或 demo 页 | 章节数在 11 与其他说法之间有争议，界面截图可以定钉 |
| 8 | 训练场 HUD：Sha-Chi 槽、两把主武器槽、Phantom Edge 槽同时可见 | best-weapons 的机制段 | 官方美术没有 HUD；解释“格挡耗槽、切武回槽”必须有真实 UI |

拍摄规格建议：4K 原生、关闭照片模式滤镜、保留 HUD、同一存档点；文件名继续用同一规则，例如 `phantom-blade-zero-white-serpent-moveset.webp`、`phantom-blade-zero-ps5-performance-vs-quality.webp`。

---

## 4. 校验结果

- 6 个页面 + 首页片段，共 **35 个 `<img>`**：全部有 `alt`、`width`、`height`，无缺失。
- 所有 `src` / `poster` / CSS `url()` 指向的文件都存在：**0 个失效引用**。
- `img/` 下 **16 张 WebP**，全部 ≤150 KB；旧 JPG 已删除。
- 全站 grep：`87/100`、`PS5 87`、`46 reviews`、`42 reviews`、`74 reviews`、`84% positive` 已无残留；`2026-11-02` 仅剩一条与控制键位参考相关的日期，与分数无关。
- 所有分数句现在只出现 **88（52）/ 86（48）/ 89 / 8.6（1,554）** 这一组。
