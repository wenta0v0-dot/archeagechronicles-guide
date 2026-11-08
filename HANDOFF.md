# ArcheAge Chronicles 指导站 — 项目简报(HANDOFF)

> 状态:**已拍板(2026-10-31)并上线**。依据:10-31 上线前竞争检查(11-3 上线,深度攻略位空位)。

## 0. 已上线(2026-10-31)

- **线上地址**:https://wenta0v0-dot.github.io/archeagechronicles-guide/
- **GitHub 仓库**:https://github.com/wenta0v0-dot/archeagechronicles-guide(公开仓,GitHub Pages「deploy from branch」)
- **技术栈**:AnvilWiki 模板(Astro 7 + MDX + Pagefind),主题色深海蓝 #1E4E79,`apply-template` 预设 2(指南型首页)
- **发布流程**:`node scripts/ship.mjs`(构建 + dist 镜像到仓库根)→ `git add -A && git commit && git push`

## 1. 站点定位(来自 10-31 竞争检查)

**上线前预占位打法**:11-3 上线(检查时剩 3 天),SERP 深度攻略位空位(仅 Reddit 帖/官方职业介绍/YouTube 视频,无专业攻略站无完整 wiki)。四职业体系 = MMO 攻略刚需。

## 2. 已验证事实红线

- 11-3 发售,$29.99,Steam,XLGames 开发
- 四职业:Warrior(Longsword/Greatsword/Gladius,招架反击)、Ranger(Hatchet/Longbow/Crossbow,风筝)、Mage(Elemental Staff/Wave Sword,AoE 法术+陨石)、Berserker(Axe+Shield/Great Axe,坦克嘲讽)
- 武器精通:武器决定技能与战斗流;切换保留原技能等级,新技能从低重练
- 洗点:消耗游戏内货币;社区建议 ~25 级锁定构筑
- **红线**:技能数值/节点/副本细节未经游戏内核验,一律不写;上线后以实机数据逐步替换

## 3. v1 内容(两页)

1. `guides/class-guide` — 四职业+武器精通+洗点规则(金钱页)
2. `guides/beginner-guide` — 上线日路线(0 小时选武器 → 25 级锁构筑)

## 4. 待办(按优先级)

1. **上线周复更**:首发补丁数据/职业数值游戏内核验后逐页替换「verified against official intros」段落
2. Search Console 验证文件(用户 Google 账号操作)
3. favicon/hero 素材换 AAC 主题
4. per-class 独立页(Warrior/Ranger/Mage/Berserker 各一篇)上线周内补

## 5. 视觉与视频更新(2026-10-31 晚)

- **电影感 Hero**:官方截图(Steam CDN 1920x1080 日落古城,无内嵌文字)做全幅背景 + 暗角渐变 + 26s Ken Burns,`public/images/hero-aac.jpg`
- **og 分享图**:换官方原画(key art 带游戏 logo),`public/images/og-aac.jpg`,1920x1080
- **预告片区**:官方预告缩略图卡片(Steam CDN)链接官方 YouTube 频道 @ArcheAgeChronicles;拿到官方预告 videoId 后替换为 LazyYouTube 内嵌播放器(`home.hero.videoId` 一行配置)

- **2026-10-31 晚补充**:Search Console 验证文件已上线(`public/googleaa0667ea4371d677.html`),待用户在 Search Console 控制台点「验证」。

## 6. 11-3 上线日观察与 v1.1 复更(2026-11-03)

- **上线状态**:Steam EA 此刻仍倒计时中,解锁 **11-3 15:00 PST / 23:00 UTC**(北京 11-4 07:00)。Steam app id **3218230**,appdetails API `coming_soon: true` 交叉验证。
- **新已验证事实**(Steam 商店页,11-3 核验):
  - 定位为 **Early Access,预计 9–12 个月**,正式版价格可能调整(Steam EA 声明)
  - buy-to-play $29.99、无订阅;XLGames 表态不出售 P2W 道具(Massively OP 10-28 报道)
  - 预购奖励 **Dawn Pioneer Outfit Chest**:主菜单按住「领取」或 [N] 键,背包开箱,领取角色绑定
  - 硬件最低:100 GB 存储 + SSD、16 GB RAM;使用 **XIGNCODE3** 内核级反作弊;AI 生成内容披露(仅作初稿)
  - EA 首发 **3 个区域**(XLGames 服务器公告 + 制作人信,10 月末)
- **上线前热度**(Next Fest Demo 10-19~10-27):Demo 数小时 20,000+ 玩家、峰值 ~19,855 SCCU、Twitch 387.5K 小时、Next Fest 首日 Top Demos + Trending Upcoming 双榜第一;社区口碑分化(UE5 画面/生活技能好评 vs 战斗手感/XIGNCODE3 争议);**无成型 meta,红线维持**。
- **v1.1 复更内容**:两篇 MDX 补 EA 定位 + 解锁时刻;beginner-guide 增「解锁时刻 + 安装/预购奖励清单」小节;class-guide FAQ 新增「Is ArcheAge Chronicles Early Access?」;`lastModified: 2026-11-03`。
- **环境备忘**:E: 盘 ACL 只读加固(Users 仅 RX),已通过 UAC 给 `E:\ArcheAgeChroniclesWiki` 单独授予勿忘 (OI)(CI)M 权限,会话写入恢复正常;撤销命令 `icacls "E:\ArcheAgeChroniclesWiki" /remove "勿忘"`(管理员)。
- **下一步**:解锁后用实机数据替换「verified against official intros」段落;per-class 独立页 ×4;跟踪解锁后首波补丁与 Steam 评价走势。

## 7. v1.2 硬性事实纠错(2026-11-04 上线日实机核验)

**背景**:上线后核查发现,预发阶段的武器名单是错的 —— **四职业错了三个**。已按首发实机数据全面改正,这是本项目首次「红线生效」的纠错记录。

### 7.1 首发武器名单(唯一权威,8 武器 / 每职业 2 把)

| 职业 | 首发武器 | 性别 |
|---|---|---|
| Warrior | Longsword, Greatsword | 仅男性 |
| Ranger | Hatchet, Longbow | 仅女性 |
| Mage | Elemental Staff, Wavesword | 仅女性 |
| Berserker | Axe and Shield, **Warhammer** | 仅男性 |

**被删掉的错误项**(旧版曾写,现已证伪):
- ❌ Warrior 的 **Gladius** —— 不是首发武器,是 **12 月更新**才加的第三把武器
- ❌ Ranger 的 **Crossbow** —— 不在首发 8 武器内
- ❌ Berserker 的 **Great Axe** —— 首发没有该选项,第二把是 **Warhammer**(多来源交叉验证:无「Berserker 用巨斧」的证据)

### 7.2 新增已验证事实(2026-11-04)

- **切换武器默认键 Q**,即时可用,可在战斗中切换
- **每把武器拥有独立的技能与 trait 进度**,同名职业不同武器 = 两套独立 build(不是同一 build 的修饰)
- **性别锁定**:Warrior/Berserker 男、Ranger/Mage 女;官方目标 1.0 前全部解除,12 月先给女性 Warrior
- **12 月更新**:Female Warrior(female 解锁第一名)+ **Gladius**(Warrior 第三把武器)
- **更新节奏**:EA 期间约每月一个大版本(制作人 Yongjin Ham 表述)
- **上线时刻修正**:实际 2026-11-03 **23:16 UTC**(上线公告时间)≈ 北京 11-4 07:16,比预告 23:00 晚 16 分钟
- **EA 期间无转服、无跨服**,建号即锁服;服务器会因人口满而锁定
- **首日故障**:部分玩家下载不启动、商店页间歇消失;**重启 Steam 可触发下载**
- **首发即已平衡**:wavesword / longbow / warhammer / elemental staff 调整;Fire Wall 削弱;Boss 增强对「最大 HP 比例伤害」的抗性
- **战斗争议已获官方承认**:耐力、受击反馈、移速、攻击打断;已指派**专职战斗团队**

### 7.3 上线首日数据快照(2026-11-04 12:45 北京)

- 同时在线:**约 20,260**(采样 20,360 / 20,272 / 20,259,轻微下行波动;已超 Demo 峰值 19,855)
- Steam 评价:**503 条,「Mixed」,52% 好评**
- 价格 $29.99,**无首发折扣**;**无 day-one 补丁**,仅上线公告
- 峰值在线无法取得:SteamDB 403、SteamCharts 500、Steam /appreviews 返回 HTML 登录墙(bot 墙)

### 7.4 教学沉淀(下次写内容必读)

1. **预发官方介绍 ≠ 首发实机**。厂商 class intro 会把「后续更新的武器」提前放进宣传物料,导致首发名单虚高。凡「首发」表述,一律以**上线后实机 + 商店页**为准。
2. **search 摘要不可直接当事实**。本次 Warhammer 与 Gladius 的差异,是靠「多来源交叉 + 反证检索(专门搜 great axe)」才确认的。
3. 两篇 MDX 现均标注 `lastModified: 2026-11-04`,正文写明「verified in-game, November 4, 2026」。

## 8. v1.3 新增排障页(2026-11-04 晚)

**动机**:上线 24 小时内玩家搜索意图从「classes/weapons」转向「卡关急救」。官方把答案埋在 Steam 公告里,无结构化、无 SEO、无中文 —— 竞争几乎为零。

- **新页**:`/guides/troubleshooting`(源 `src/content/wiki/en/guides/troubleshooting.mdx`)
- **素材来源**:官方公告 *[Notice] Key Issues on Early Access Launch Day and Our Response Plan*(2026-11-04 10:57 UTC)+ *Temporary Maintenance Notice*(2026-11-04 14:10 UTC)
- **结构**:顶部「Quick fix sheet」速查表(症状 → 状态 → 做法),下接 Accordion 分组详情(阻断进度 / 脱困 / 设置建议 / 维护与平台),每条形目带**状态标签**(已修复待部署 / 调查中 / 有临时方案 / 仅能提工单)
- **互链**:两篇旧指南的「What to read next」均已加入该页;新页回链两篇 + `/tags/launch/`
- **官方已确认清单**(勿重复造谣):tutorial 卡住、Boss 离开区域后不刷新、Malchuk 死亡后不出现/无法复活、NPC 对话后断链(含 Cliffs of Madness)、队伍解散/队长离开卡副本、**钥匙不共享需各自拾取**、卡地形(ESC→Escape,不行重启)、反作弊初始化卡死(提工单)、Linux/Steam Deck **不支持**、优化中
- **维护窗口**:11-4 09:00 PT = 17:00 UTC = 北京 **11-5 01:00**,约 2 小时
- **数据快照(11-4 23:24 北京)**:在线 19,078;评价 1,371 条 Mixed 52%(与 12:45 的 503 条 52% 持平);峰值据报道 ~26,000

**下一轮复更触发条件**:① tutorial/Boss 修复正式部署 → 重写状态列与临时方案;② 12 月更新(female Warrior + Gladius)→ 更新 class-guide;③ 评价跌破/回升至明显档位(如 Mostly Negative / Mostly Positive)→ 首页文案跟进。

## 9. v1.4 复更:维护补丁落地 + 触发条件 ① 命中(2026-11-06)

**触发条件 ①(tutorial/Boss 修复部署)部分命中** → troubleshooting 页已更新(`lastModified: 2026-11-06`)。

### 11-4 维护实际上线内容(公告 11-4 19:53 UTC,北京 11-5 03:53)

- ✅ **教程进度修复**(launch-issue 清单第 1 项 → 已部署)
- ✅ **Meliot 不出现修复**(注意:这是具体案例,通用「离开区域 Boss 不刷新」修复未在补丁说明中确认 → 页面状态改为 Partially fixed,建议维持「打完再走」)
- ✅ Altar of Seals 重试修复;私聊显示修复;Krogal 命中判定改进
- ✅ Diamond Shores 四任务可放弃(Weeping Dead's Doll / Gnoll's Doll / Seaglass Beach Lantern's Calling / Watcher's Village Lantern's Calling)
- ✅ Hereafter Stone 禁售(可弃);Cheap Moonshine 可弃;拆解设置调整;冲突频道 Pioneer's Assembly Hall 禁止互攻
- **客户端更新提示**:Steam 库更新;无更新按钮 → 完全关闭重启 Steam(页面已写入 Callout)

**仍调查中(官方未再更新)**:Malchuk、通用 Boss 重置、NPC 对话断链(含 Cliffs of Madness)、队伍解散卡副本。

### 其他新事实

- **封禁公告**(11-5 10:19 UTC):首波对「系统漏洞异常使用」账号执行制裁,持续监控并将续报 —— 仅观察记录,不作内容(政策猜测踩红线)
- **评价**:总推荐 2,559(11-5 16:48 UTC);全语言档位仍 **Mixed**;**英文子集 67% 好评**(1,015 条)—— 逼近 Mostly Positive 线(70%),触发条件 ③ 未命中但需盯
- **在线**:13,471(11-5 16:48 UTC);曲线:20,360(11-4 12:45)→ 19,078(11-4 23:24)→ 13,471(11-5 16:48)≈ 3 天 -34%
- 维护公告里把客户端重启写进官方指引,与页面既有「下载不启动→重启 Steam」提示互证

### 触发条件更新

1. ~~tutorial 修复部署~~ → **已处理(本次)**
2. 通用 Boss 重置 / Malchuk / 散队卡副本修复确认 → 再更状态列
3. 评价档位变化(英文子集 67% 很接近 70% 的 Mostly Positive 线,随时可能翻转)→ 首页/文案跟进
4. **新增**:12 月更新(female Warrior + Gladius)官方细节公布 → class-guide

## 10. 同行分析与 v1.5:借鉴竞品内容(2026-11-06 晚)

### 竞争格局快照

- **Wikily.gg**:全品类数据库(交互地图/掉落率/任务链/物品)+ 手机与游戏内悬浮窗 App —— 重型对手,不正面竞争
- **MetaForge**:内容站,known-issues 页与新手指南页**已进排名** —— 我们排障页的直接对标
- **AOEAH / LAGOFAST / SSEGOLD**:RMT 内容营销,tier list 导流
- **ArcheAgeBuilds.com**:同型垂直站;**Fandom wiki 仅 26 页纯 lore,胚胎期**
- 本站建站 6 天,尚未进前页(新域正常)

### v1.5 借鉴内容(均标注来源与「非官方」)

- troubleshooting 新增 **「Launch, black screen, and crash fixes」** 7 步清单(首次启动 shader 编译等待 ~10 分钟 / 全退 Steam 杀进程 / 关覆盖层 / 验证文件 / XIGNCODE3 隔离区 / GPU 驱动 / Intel NPU 崩溃解法)—— 来源 MetaForge(11-4)+ LagZapper
- troubleshooting 新增 **「Dungeon boss missing — leader-swap trick」**:换队长 → 全员退副本 → 重进,**标 community-reported + 链接 Steam 讨论区原帖**,并写明未经验证
- 键位重绑条目补充:目前可重绑 ~10 个 UI 快捷键 + 分设备反转 Y 轴(MetaForge)
- 平台条目补充:Proton/改文件有**封号风险**(反作弊),Family Sharing 官方不支持
- beginner-guide 安装清单补:首次启动黑屏 ~10 分钟属正常;Family Sharing 不支持;内核级反作弊
- FAQ +2:「won't launch / black screen」「dungeon boss never spawns」
- **未收录**:「第一副本隔栏杆对话 + 水下钥匙」技巧 —— 搜索摘要提到但无稳定来源,标记为待核实线索

### 待办(源自同行分析)

1. **tier-list 新页**(抄 AOEAH 数值化格式 + Quick Picks,红线内标注来源)—— 上线周最大流量词缺口
2. per-class ×4 时把「trait 点数 ~95 / 单武器 50-60」这类社区数据以 reported 标签纳入
3. Wikily 式关联互链密度:per-class 页之间武器↔职业↔构建互链

## 11. ⚠️ CI 自 11-2 起持续红(历史遗留,非本次引入)(2026-11-06)

**发现**: Actions 里 `CI` workflow **每次推送都 failure**(至少从 11c5b906/11-2 起,含 11-3/11-4/11-5/11-6 全部 5 次推送)。**Pages 部署不受影响**(deploy from branch 独立走,全部 success),线上一直正常。

**失败范围**:两个 job 全挂
- `check` → "Quality gates" composite(八道门折叠成一个 step,远程看不到具体哪道)
- `ops-toolkit` → tools/anvil-ops 的 typecheck+test+build(本会话从未触碰该目录)

**本地复现**:八道门(含 `--strict-ui`)+ `pnpm install --frozen-lockfile` 在 Windows 本地全绿 → 疑似环境差异:
1. gates action 的 `site-url` 用 `${{ vars.SITE_URL || 'https://anvil.wiki' }}` —— 若 repo vars 没配 SITE_URL,远程构建用的是模板默认域,后续 check-links/check-sitemap 可能因此挂
2. ubuntu(Node 走 .nvmrc)与本地 Windows 的差异
3. ops-toolkit 自带 lockfile 的独立安装

**诊断被阻塞**:共享出口 IP 的 GitHub API 配额耗尽(runners/logs 接口 403/429),gh CLI 未安装。

**下一步选项**:
- 用户登录浏览器打开 Actions → 最新 CI run → 贴出失败 step 的日志尾部(最快)
- 或等 IP 配额窗口重置后用 API 拉 logs zip
- 修复时优先检查 repo Settings → Variables → actions 有无 `SITE_URL`

## 12. v1.6:tier-list 新页 + 11-7 补丁 + 评价翻档(2026-11-08)

### 触发条件 ② 命中:评价翻档

- Steam 全语言标签 **mixed → positive**(2026-11-08 11:01 UTC 抓取:英文子集 **71% 好评,1,588 条**;总推荐 4,049)
- 轨迹:52%(503,11-4)→ 67%(1,015,11-5)→ 68%(1,204,11-6)→ **71%**(1,588,11-8),稳步爬升
- **首页文案跟进方式**:hero/meta/overview 三处 description 刷新 —— 「verified against official class intros」(已过时)→「verified in-game and dated」,并把 known-issues tracker 写进站点定位。未把评价数字写上首页(会快速腐烂,与 dated 原则冲突)

### tier-list 新页(/guides/tier-list,竞品分析 #2 落地)

- **素材**:AOEAH launch-week tier list(11-4)全 12 武器 PvE/PvP 评分(8 实装 + 4 projected:Gladius/Great Shield/Crossbow/Vitality Staff)+ 5 PvE + 5 PvP 社区 build
- **红线执行**:页面顶部 warn Callout 明示「community-sourced,not verified in-game by this site」,全表标注来源与日期;projected 行带 * 并注明仅 Gladius 有官方日期(12 月)
- **结构**:班级评分表 → 武器 12 行表 → 两条结构解读(Longsword 专精化 / Warhammer 垫底但有刚修复的 bug)→ Quick Picks by playstyle(PvE/PvP)→「为什么底部先动」(Warhammer trait 修复 / 战斗手感重做 / **trait 点数 exploit 已关闭并强制重置**)→ 变动预告(12 月 Gladius 落地即重排)
- 互链:class-guide(正文+What to read next)、troubleshooting、beginner-guide、/tags/builds/;beginner-guide 与 class-guide 已回链

### 11-7 补丁(08:30 UTC)—— 站点状态列更新

- **Cliffs of Madness 断链已修**:Poldat 后可重进区域找入口处 Kevin(排障页状态:Partially fixed (Nov 7),FAQ +1)
- **聊天隐藏选项已上线**(Options 内开关 mini chat + 频道通知选择)—— 原「计划中」条目改为已交付
- 重生改进:Revive Nearby (F) / Go Outside (G);仓储 200→1,000
- **trait exploit 关闭**:Collapsed Southern Ruins 的 Recommended Traits 强制分配点数已重置(写入 tier-list「底部先动」+ class-guide launch-week)
- 战斗:Warhammer Unstoppable Force II 不再叠层、Reckless Destroyer / Ice Crystal 修复、Bauchu 地形奶酪移除
- Malchuk:通道进出修复 + 重生改进(**核心「死后不重现」仍未确认修复**,状态维持 Under investigation 并注明部分缓解)

### 数据快照(11-8 19:01 北京)

在线 12,993(11-6 23:15 为 14,135);评价 4,049 条;价格 $29.99 无折扣;11-7 后暂无新公告

### 触发条件(下一轮)

1. ~~评价翻档~~ ✅ 已处理(文案刷新)
2. Malchuk / 通用 Boss 重置 / 散队修复确认 → 排障页状态列
3. **12 月更新细节**(female Warrior + Gladius)→ class-guide + tier-list 重排
4. **AOEAH 等 tier list 更版**(11-4 版已旧)→ tier-list 换源/重日期
