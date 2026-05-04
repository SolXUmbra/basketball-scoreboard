# 🏀 Basketball Scoreboard for OBS Live Streaming

<p align="center">
  <img src="https://img.shields.io/github/license/SolXUmbra/basketball-scoreboard?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square" alt="PRs Welcome">
  <img src="https://img.shields.io/badge/OBS-Browser%20Source-blue?style=flat-square" alt="OBS Compatible">
</p>

> Real-time basketball game scoreboard overlay for OBS live streaming. Works as a browser source — no install, no dependencies.

**[中文说明见下方](#篮球比赛obs直播比分栏)**

---

## Preview

```
┌─────────────────────────────────────────────────────┐
│  [bg color]  FIBA 3x3 Basketball  [text color]      │  ← Title bar
├─────────────────────────────────────────────────────┤
│ [jersey] [Team A Name]  [Foul] [Score]             │  ← Home team
│ [jersey] [Team B Name]  [Foul] [Score]             │  ← Away team
└─────────────────────────────────────────────────────┘
```

Design: 8° left tilt for dynamic sports feel.

## Features

| Action | Effect |
|--------|--------|
| Click **left** of score/foul cell | -1 |
| Click **right** of score/foul cell | +1 |
| Double-click any text area | Edit inline |
| Click color dot | Change color |
| Click empty area / Press Enter | Exit edit mode |

### Customizable

- **Game title** — double-click to edit
- **Team names** — double-click to rename
- **Scores** — click ±1
- **Foul counts** — click ±1
- **Jersey colors** — 16-color palette
- **Team background / text colors** — 16-color palette
- **Title background / text colors** — 16-color palette

## Quick Start

### Option 1: OBS Browser Source (Recommended)

1. Download `scoreboard.html` from this repo
2. Open OBS → **Sources** → **+** → select **Browser**
3. Configure:

| Setting | Value |
|---------|-------|
| Local file | ✅ checked |
| File path | path to `scoreboard.html` |
| Width | 1920 |
| Height | 1080 |
| Custom CSS | `body { background: transparent; }` |
| FPS | 30 |

4. Drag to bottom-left corner (or any position)
5. Recommended resolution: 1280×720 or 1920×1080

### Option 2: Direct Browser Preview

Open `scoreboard.html` in Chrome/Edge directly.

### Option 3: Other Streaming Software

Add OBS window capture or browser source to your streaming software.

## 16-Color Palette

| # | Color | Preview |
|---|-------|---------|
| 1 | `#FFFFFF` | ⬜ White |
| 2 | `#bdc3c7` | ⬜ Silver |
| 3 | `#7f8c8d` | ⬜ Gray |
| 4 | `#2d3436` | ⬛ Charcoal |
| 5 | `#d63031` | 🟥 Red |
| 6 | `#e67e22` | 🟧 Orange |
| 7 | `#f1c40f` | 🟨 Yellow |
| 8 | `#FFD700` | 🟨 Gold |
| 9 | `#2ecc71` | 🟩 Green |
| 10 | `#00b894` | 🟩 Teal |
| 11 | `#0984e3` | 🟦 Blue |
| 12 | `#192a56` | 🟦 Navy |
| 13 | `#6c5ce7` | 🟪 Purple |
| 14 | `#e84393` | 🟪 Pink |
| 15 | `#00cec9` | 🟩 Cyan |
| 16 | `#1e272e` | ⬛ Near-black |

## Keyboard Shortcuts

```
Score +1   → Click right side of score area
Score -1   → Click left side of score area
Foul +1    → Click right side of foul area
Foul -1    → Click left side of foul area
Edit text  → Double-click → type → Enter or click outside
Change color → Click side dot → pick color → click elsewhere
```

## Use Cases

- 🏀 Campus / school basketball games
- 🏀 Corporate / community leagues
- 🏀 3x3 basketball (FIBA 3x3)
- 🏀 Exhibition games and training sessions

## Layout

```
┌─────────────────────────────────────────────────────┐
│  [bg]  Game Title (double-click to edit)  [text]   │
├─────────────────────────────────────────────────────┤
│ [jersey] [Team Name]  [Foul] [Score]               │
│ [jersey] [Team Name]  [Foul] [Score]               │
└─────────────────────────────────────────────────────┘
Overall: 8° left tilt
```

## Customize Defaults

Edit `scoreboard.html` to change defaults:

| Item | Location in source |
|------|---------------------|
| Game title | `id="title-input" value="..."` |
| Home team name | `id="h-n-input" value="..."` |
| Away team name | `id="a-n-input" value="..."` |
| Home score | `id="h-score" value="0"` |
| Away score | `id="a-score" value="0"` |
| Home fouls | `id="h-foul" value="0"` |
| Away fouls | `id="a-foul" value="0"` |
| Home jersey color | `fill="#..."` (SVG path) |
| Away jersey color | `fill="#..."` (SVG path) |

## Tech Specs

| Item | Value |
|------|-------|
| File type | Single HTML file, zero dependencies |
| Browser | Chrome, Edge, Firefox, Safari |
| Background | Transparent |
| Font | Impact + Microsoft YaHei (system fonts) |
| OBS support | Browser Source ✅ |
| File size | ~12KB |

---

## 🏀 篮球比赛OBS直播比分栏

适用于各类篮球比赛转播的实时比分栏，可直接作为 OBS 浏览器源叠加到直播画面使用。

### 功能一览

#### 基础操作

| 操作 | 效果 |
|------|------|
| 点击分数/犯规单元格**左侧** | -1 |
| 点击分数/犯规单元格**右侧** | +1 |
| 双击文字区域 | 进入编辑模式，直接输入 |
| 点击颜色选择器圆点 | 更换对应颜色 |
| 点击空白处 / 按 Enter | 退出编辑 |

#### 可调整内容

- **赛事标题**：双击标题区域修改赛事名称
- **球队名称**：双击球队名单元格，修改为自定义内容
- **分数**：点击计分区域左右两侧 ±1
- **犯规次数**：点击犯规区域左右两侧 ±1
- **球衣颜色**：点击球衣格左侧区域，弹出 16 色调色板
- **球队背景色**：点击球队名左侧区域，选择背景色
- **球队文字色**：点击球队名右侧区域，选择文字颜色
- **标题背景色**：点击标题左侧区域，选择标题背景
- **标题文字色**：点击标题右侧区域，选择标题文字颜色

## 完整使用教程

### 方式一：OBS 浏览器源（推荐）

1. 下载本仓库 `scoreboard.html`
2. 打开 OBS，点击 **「来源」** 面板 → **「+」** → 选择 **「浏览器」**
3. 设置如下：

| 设置项 | 推荐值 |
|--------|--------|
| 局部文件 | 打勾 ✅ |
| 文件路径 | 指向 `scoreboard.html` |
| 宽度 | 1920 |
| 高度 | 1080 |
| CSS 自定义 | `body { background: transparent; }` |
| FPS | 30 |

4. 将来源拖到画面左下角（或你想要的任意位置）
5. 建议解析度：1280×720 或 1920×1080

### 方式二：直接浏览器预览

直接双击 `scoreboard.html` 用 Chrome/Edge 打开即可操作。

### 方式三：直播姬 / 斗鱼等平台

将 OBS 窗口捕获或浏览器源添加到直播软件中。

## 16 色调色板

点击颜色区域侧边弹出的圆点，对应颜色如下：

| 序号 | 色值 | 预览 |
|------|------|------|
| 1 | `#FFFFFF` | ⬜ 白 |
| 2 | `#bdc3c7` | ⬜ 银灰 |
| 3 | `#7f8c8d` | ⬜ 深灰 |
| 4 | `#2d3436` | ⬛ 炭黑 |
| 5 | `#d63031` | 🟥 大红 |
| 6 | `#e67e22` | 🟧 橙色 |
| 7 | `#f1c40f` | 🟨 黄色 |
| 8 | `#FFD700` | 🟨 金色 |
| 9 | `#2ecc71` | 🟩 绿色 |
| 10 | `#00b894` | 🟩 青绿 |
| 11 | `#0984e3` | 🟦 蓝色 |
| 12 | `#192a56` | 🟦 深蓝 |
| 13 | `#6c5ce7` | 🟪 紫色 |
| 14 | `#e84393` | 🟪 粉色 |
| 15 | `#00cec9` | 🟩 青色 |
| 16 | `#1e272e` | ⬛ 近黑 |

## 快捷操作汇总

```
分数 +1   → 点击计分区右侧
分数 -1   → 点击计分区左侧
犯规 +1   → 点击犯规区右侧
犯规 -1   → 点击犯规区左侧
编辑文字  → 双击该区域 → 输入 → 回车或点击外部确认
换颜色    → 点击区域侧边 → 选颜色 → 点击其他区域关闭
全屏编辑  → 点击 OBS 里的浏览器源，调整窗口大小
```

## 适用场景

- 🏀 校园篮球赛直播
- 🏀 企业/社区联赛直播
- 🏀 三人篮球赛（FIBA 3x3）
- 🏀 友谊赛、训练赛

## 布局说明

```
┌─────────────────────────────────────────────────────┐
│  [背景色]  赛事标题（双击编辑）  [文字色]            │  ← 标题行
├─────────────────────────────────────────────────────┤
│ [球衣] [球队名称（双击编辑）] [犯规] [分数]          │  ← 主队
│ [球衣] [球队名称（双击编辑）] [犯规] [分数]          │  ← 客队
└─────────────────────────────────────────────────────┘
```

整体向左倾斜 8°，增加动感设计感。

## 自定义扩展

如需修改预设内容，直接编辑 `scoreboard.html` 源码中对应的 `value` 属性即可：

| 位置 | 源码位置 |
|------|----------|
| 赛事标题 | `id="title-input" value="..."` |
| 主队队名 | `id="h-n-input" value="..."` |
| 客队队名 | `id="a-n-input" value="..."` |
| 主队分数 | `id="h-score" value="0"` |
| 客队分数 | `id="a-score" value="0"` |
| 主队犯规 | `id="h-foul" value="0"` |
| 客队犯规 | `id="a-foul" value="0"` |
| 主队球衣色 | `fill="#..."` (SVG path) |
| 客队球衣色 | `fill="#..."` (SVG path) |

## 技术参数

| 项目 | 说明 |
|------|------|
| 文件类型 | 纯 HTML（单文件，无外部依赖） |
| 浏览器兼容 | Chrome、Edge、Firefox、Safari |
| 背景 | 透明（PNG 32位可直接叠加） |
| 字体 | Impact + Microsoft YaHei（系统自带） |
| 交互方式 | 鼠标点击 + 触屏 |
| OBS 支持 | 浏览器源 ✅ |
| 文件大小 | ~12KB（极轻量） |
