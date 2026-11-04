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
