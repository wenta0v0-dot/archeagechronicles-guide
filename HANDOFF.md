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
