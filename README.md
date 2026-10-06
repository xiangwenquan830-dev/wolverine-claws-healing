# Wolverine: Claws & Healing · 金刚狼：钢爪与自愈

![Cover](wolverine-cover.png)

**本模组由 AI 辅助制作。 / This mod was created with AI assistance.**

**Minecraft 1.20.1 · Forge 47.4.0+ · Java 17 · r67 Beta**

[下载 r67 / Download r67](https://github.com/xiangwenquan830-dev/wolverine-claws-healing/releases/tag/r67)

## 中文介绍

注射金刚狼血清，永久获得随角色保存的再生能力与艾德曼合金钢爪。能力在死亡重生和重新登录后保留，不依赖指定护甲。

- 钢爪战斗：双爪、单爪与符合条件的持物组合，三段连招、重击和飞扑。
- 自动自愈：基础恢复、再生储备与低血量恢复机制；高额瞬间伤害仍可能致命。
- 格挡与反击：普通格挡积累负担，精准格挡提供反击机会。
- 墙面移动：攀爬、横移、单爪悬挂与满足碰撞条件的翻越。
- 第一、第三人称钢爪表现、声音反馈、可配置 HUD 与身体伤口显示。
- 包含枪爪相关兼容路径；第三方枪械、特殊枪臂及整合包仍需逐项实测。Better Combat 为可选兼容，不是必需依赖。Darwin Soldier 桥接不代表无视其闪避或战斗直觉。

## r67 更新


- 改进高低沿、断层、缺口、垛口及边角的抓沿搜索，根据实际碰撞形状寻找可达抓点。
- 正前方无法落脚时，尝试附近左右安全落点；保留完整脚底支撑和身体路径检查。
- 单手悬挂转正后，只有取得两个真实抓点并通过路径检查才转为双手翻越。
- 动态障碍导致取消后，持续同次输入不再反复重启；松开前进后重新按下可重试。
- 保留碰撞、局部搜索预算及原有翻越时长。相对 r66 不改枪爪、自愈、伤口素材、伤害、攻速、格挡和达尔文联动。


## 安装与验证范围

备份存档与配置，退出游戏，将旧金刚狼 JAR 移出 mods，只放入 `wolverine-forge-1.20.1-r67.jar`。客户端与服务器使用匹配版本，保留原有配置与能力数据。ZIP 不放入 mods。

**Beta：**随附 r67 记录报告正式构建与离线回归通过；本次发布核对了版本、文件大小与 SHA-256，未重新执行构建或游戏测试。真实客户端、专用服务器、多人联机、中文 Windows 与用户整合包仍未完成本轮实机验收。

## English

Inject Wolverine serum to unlock persistent claws and regeneration. Fight with claw combos, heavy attacks and pounces, block and parry, climb walls and mantle when collision checks allow. Includes first- and third-person presentation, configurable HUD, and visible healing wounds.

r67 improves reachable ledges around gaps and corners, searches nearby safe landing positions, validates one-hand-to-two-hand transitions, and prevents repeated restart after blocked mantles. Collision and support checks remain. Combat, healing, wound art and other features are unchanged from r66.

Use Minecraft 1.20.1, Forge 47.4.0+ and Java 17. Back up your world and settings, remove the previous JAR, and install only the new JAR. Match client/server versions. Keep ZIP archives out of mods.

**Beta testing status:** supplied delivery records report a successful build and offline regression checks. This publication verifies version and artifact hashes only; actual client, dedicated-server, multiplayer, Chinese Windows and modpack testing remains outstanding for this iteration.

## 文件与许可 / Files and license

- `wolverine-forge-1.20.1-r67.jar`：安装文件 / playable mod binary.
- `wolverine-forge-1.20.1-r67-project.zip`：作者提供的 r67 工程导出，含源码与随附资料。它不是交付说明中单独列出的 development ZIP；未独立验证完整可复现构建。 / Supplied r67 project export, including source and accompanying materials; not the separately documented development ZIP. Reproducible build completeness has not been independently verified.
- GitHub 自动生成的 Source code 压缩包只包含本仓库说明和封面，不是模组工程。 / GitHub's automatic source archives contain this documentation repository, not the mod project.

JAR SHA-256: `6701986ea19f26e26c3869dc6cb3a75796b2c1e0d684b0545d95b80a0c930465`

模组元数据声明 All Rights Reserved；JAR 内第三方声明继续适用。 / Mod metadata declares All Rights Reserved; bundled third-party notices still apply.

