# 金刚狼：钢爪与自愈

![Cover](wolverine-cover.png)

[Download r34 Beta](https://github.com/xiangwenquan830-dev/wolverine-claws-healing/releases/tag/r34)

# Wolverine: Claws & Healing · 金刚狼：钢爪与自愈

**Minecraft 1.20.1 · Forge 47.4.0+ · Java 17**

Inject Wolverine serum to permanently unlock steel claws and regeneration. Your abilities persist through death and relogging without requiring special armor.

## Features

- **Adaptive claws:** fight with two empty hands, a single available hand, or a supported one-handed melee weapon plus an offhand claw. Occupied hands follow compatibility rules; freeing a hand restores its claw while claw mode remains enabled.
- **Claw combat:** three-hit combos, a separate heavy attack, pouncing, attack-speed-aware timing, and a default reach bonus of one block above your effective base reach.
- **Armor penetration and shield breaks:** normal claws and pounces ignore 45% of armor by default; heavy attacks ignore 75%. Eligible blocked finishers or heavy attacks can disable a shield for 3 seconds, with a 6-second shield-break cooldown. Other damage reduction and dodge mechanics still apply.
- **Automatic healing:** default free healing is 5% of maximum health per second; total combat healing is 20%, and total out-of-combat healing is 35%. These totals include the free portion. Additional healing costs regeneration reserve, which replenishes out of combat.
- **Survival under pressure:** low health and severe injuries accelerate healing, subject to a default 50%-of-max-health-per-second cap. Conditional near-death healing bursts are not resurrection; lethal burst damage can still kill you.
- **Blocking and parrying:** default normal damage reduction is 70% with two claws and 45% with one. Blocking builds burden and can break your guard. A successful perfect parry negates eligible damage and reduces existing burden.
- **Wall movement:** climb, move sideways, descend while sneaking, hang from one claw, catch nearby surfaces while falling, and mantle where collision and landing checks allow. Release jump to detach. Grip checks use block collision shapes.
- **Presentation:** first- and third-person claw animations, combat sounds, and a compact configurable HUD.

## r34 highlights

The new default perfect-parry window is **6 ticks (about 0.3 seconds)**. Equipment identity checks better tolerate changing item data such as energy or heat. Dense-scene targeting prioritizes the crosshair and forward targets instead of abandoning all attacks when a broad candidate query exceeds 64 entities. Independent obstruction checks remain in place; some historical sweep assistance is reduced in extremely dense scenes.

Existing saves retain their previous parry configuration. A previous 4-tick setting must be adjusted manually or migrated using the available one-time migration option.

## Compatibility

**Better Combat is optional**, not required. Unsupported versions or changed interfaces may disable parts of the bridge. Special weapon behavior may require individual support.

The **Darwin Soldier** bridge lets eligible direct player claw melee participate in related checks. It does not bypass combat intuition or grant claw bonuses to bullets and other indirect damage. Skill combinations still require testing.

**Automatic gun-and-claw mixed combat is not included in r34.**

## Installation and testing status

Back up your world and configuration, remove the old Wolverine JAR, and place only the new JAR in your mods folder. Use matching versions on clients and the server. Preserve existing ability data and configuration. Source ZIPs do not belong in the mods folder.

**Beta:** the author's delivery notes report build and offline regression checks. Real single-player, dedicated-server, and multiplayer acceptance testing remains incomplete. Animation feel, latency, modpacks, and third-party combinations need in-game validation.

---

# 中文介绍

注射金刚狼血清，永久获得随角色保存的再生能力与艾德曼合金钢爪。能力在死亡重生、重新登录后保留，不依赖指定护甲。

## 艾德曼合金钢爪

钢爪是身体能力，不作为普通武器占据快捷栏。进入伸爪模式后，可用空手自动伸爪；持物时对应手暂停，重新空手后恢复。

- 双手空置：使用双爪。
- 主手空、副手持物：使用主手爪。
- 主手持符合条件的单手近战武器、副手空：支持武器与副手爪混合攻击。
- 双手武器及其他占手状态按兼容规则限制，不强行抢占物品操作。

提供空手槽保护、三段普通连招、独立重击与飞扑。命中时机随有效攻速调整；普通攻击具有短暂命中窗口和移动扫掠检测。默认攻击距离在玩家有效基础距离上额外增加 **1格**。

钢爪伤害结合招式基础值与玩家攻击属性，按规则排除持物专属加成，避免直接叠加完整剑伤。

| 攻击类型 | 默认忽略护甲比例 |
| --- | --- |
| 普通爪击及飞扑 | 45% |
| 独立重击 | 75% |

破甲只作用于当次护甲计算，不永久降低目标护甲，也不等于无视抗性、附魔减伤或其他模组闪避。

符合条件的终结爪击或重击被盾牌实际挡住后，可禁盾 **3秒**，破盾冷却 **6秒**。当次仍按正常盾牌格挡处理，不追加伤害，也不直接破除其他模组的战斗直觉。

## 自愈与再生储备

自动按最大生命值比例恢复，可适应额外生命值加成。

| 状态 | 默认每秒恢复最大生命值 |
| --- | --- |
| 免费基础恢复 | 5% |
| 战斗状态总恢复 | 20% |
| 脱离战斗总恢复 | 35% |

总速度已包含免费基础部分。每额外恢复 **1%最大生命值**，默认消耗 **0.25点储备**。满血不无故消耗，接近满血优先免费恢复；储备不足保留基础自愈，脱战后逐渐补充储备。费用根据实际额外治疗量结算，并考虑治疗事件被取消或修改。

低血量和重伤会加速恢复，默认总恢复上限为每秒最大生命值的 **50%**。符合血量、储备和冷却条件时可触发短暂濒死恢复爆发；这不是自动复活，高额瞬间伤害仍可能致命。低血量额外减伤默认最高 **45%**。第三方特殊负面效果仍需检查兼容。

## 格挡与精准反击

钢爪能格挡符合条件的正面近战和远程攻击。双爪普通格挡默认减伤 **70%**，单爪 **45%**。普通格挡积累负担，达到上限会破防。

r34新配置默认精防窗口为 **6 tick，约0.3秒**。成功精防使符合条件的当次伤害归零，不增加负担，默认减少 **15点已有负担**，并提供短暂反击机会。保留触发间隔和奖励次数限制，不能靠反复举爪无限刷新。

**旧存档保留原配置。** 原来为4 tick时，需手动调整或启用一次性迁移才能使用6 tick窗口。

## 飞扑与墙面移动

飞扑默认最大位移 **8格**，服务器检查目标、位移、碰撞与命中；遇到目标、障碍或条件失效时提前结束，不穿墙、不直接传送。

支持正面双爪攀爬、沿墙横移、潜行下移、侧身单爪悬挂，以及下落时抓住身旁有效表面。松开跳跃脱离墙面。单双爪状态根据接触持续判断。

抓点使用实际碰撞形状，栅栏、铁栏杆、石墙、玻璃板等可参与判断。翻顶需要可用抓沿、通过空间和安全落点；窄栏杆可寻找另一侧落点。门打开、抓点拆除或落点阻挡后重新判断。第三方建筑方块仍取决于碰撞形状及适配。

## 动画、音效与界面

提供第一、第三人称伸收爪、连招、格挡、飞扑和攀爬动作，以及金属、命中和移动反馈。紧凑HUD显示储备与战斗状态，部分声音、HUD和视觉反馈可配置。攻击与自愈由游戏逻辑处理，不依赖渲染帧率决定伤害次数。

## r34重点改进

- 新默认精防窗口扩大至6 tick，保留成功奖励。
- 统一装备身份及战斗状态判断，减少能量、热量等动态数据误中断。
- 密集选敌不再因宽范围候选超过64个就放弃全部攻击。
- 优先准星与前方目标，保留独立遮挡检查。
- 延续攀爬异常、普通武器冷却及爪击容错修复。

极密集场景会减少历史扫掠等辅助检测，优先保留基础正面攻击。

## 模组兼容

**Better Combat为可选兼容，不是必需依赖。** 未安装仍有独立战斗路径；未知版本或结构变化可能停用部分桥接，特殊武器需要逐项适配。

**Darwin Soldier**桥接主要让符合条件的直接玩家钢爪近战参与相关最低伤害及技能判定，不让子弹获得钢爪加成，也不无视战斗直觉。全部技能组合仍需实测。

**枪爪智能混合模式不包含在r34中。**

## 安装与更新

1. 使用 **Minecraft 1.20.1、Forge 47.4.0或更高的1.20.1版本、Java 17**。
2. 备份存档及配置，移出旧金刚狼JAR，只保留一个版本。
3. 新JAR放入mods文件夹；客户端和服务器使用匹配版本。
4. 保留原有能力数据与配置，无需删档重新获得能力。
5. 源码ZIP不要放入mods。
6. 旧存档按需要将精防窗口调整为6 tick。

## 验证范围

根据作者提供的交付说明，r34记录了构建与离线回归结果。这不代表所有整合包均已验证。**真实单人、专用服务器与多人联机验收尚未完成**，动画手感、延迟及第三方模组组合需要实际游戏验证。

## Repository contents / 仓库内容

This repository distributes the r34 binary and documentation. Matching r34 source has not been supplied. The separately supplied source archive was identified as r33 and is not presented here as r34 source. GitHub automatically generated source archives contain this repository documentation, not the mod source.

本仓库提供 r34 成品与说明。当前提供的源码材料为 r33，因此未当作 r34 源码上传；GitHub 自动生成的源码压缩包仅包含本仓库文档。

The mod metadata declares All Rights Reserved. Third-party notices bundled in the JAR continue to apply. / 模组元数据声明保留所有权利，JAR 内第三方声明仍适用。
