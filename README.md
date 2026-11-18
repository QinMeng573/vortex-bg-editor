# 旋涡背景编辑器 · Vortex Background Editor

一款小丑牌式（Balatro-style）流体旋涡背景的开源调参编辑器。单文件、零依赖、双击就能用：
7 种运动模式共用同一套流体域扭曲（domain-warp）渲染管线，只切换运动方式——调模式、调预设、
调全部参数，还带会自己变色的颜色脚本。调好后复制参数 JSON，或一键导出独立 HTML 嵌进你的游戏/网页。

A Balatro-style fluid vortex background editor. One single HTML file, zero dependencies.
Seven motion modes share one domain-warp shader pipeline; tune every parameter, let the colours
animate themselves, then copy the JSON config or export a standalone HTML background.

## 功能 Features

- **7 种运动模式（同一引擎，只换运动块）**：旋涡 Vortex / 涟漪 Ripple / 烟雾旋涡 Smoke Swirl / 波涌 Wave / 潮汐呼吸 Tide / 圣光放射 Rays / 万花筒 Kaleido
- **13 套自创预设**：含《国王棋》主菜单蓝白定版与战斗绛红涟漪定版；点预设时三色以 0.8 秒平滑渐变过渡，绝不突变
- **全部参数可调**：主色/亮色/暗色、对比度、旋转量、速度、像素细腻度、旋转缓动、运动强度、运动速率、涟漪频率/速率/幅度（仅涟漪模式）、中心闪光、中心偏移
- **颜色脚本（自动变色，全程 HSL 最短路径平滑插值）**：
  - 颜色时间轨迹：给主色/亮色各排一条关键帧轨道，循环渐变
  - 颜色池：随机抽色平滑过渡，可调停留与过渡时长
  - 双色自动轮播：成对配色轮换，可调停留与过渡时长
- **参数 JSON 互通**：复制/粘贴导入导出，格式与《国王棋》游戏内调参台完全一致，调好的参数可直接移植进游戏
- **一键导出独立 HTML**（只有背景、没有面板）、**导出 PNG 快照**、随机配色、暂停、按 H 隐藏面板
- **双渲染路径**：WebGL 不可用时自动降级 Canvas 2D 备用渲染，绝不白屏

## 使用 Usage

1. 在线演示：见仓库 GitHub Pages（仓库主页右侧链接）
2. 本地使用：下载 `index.html`，双击用浏览器打开即可，无需服务器、无需安装

参数 JSON 格式示例：

```json
{
  "mode": "vortex",
  "c1": "#1D4ED8", "c2": "#FFFFFF", "c3": "#081226",
  "contrast": 3, "spinAmount": 0.6, "speed": 0.5,
  "pixelSizeFac": 2000, "spinEase": 0.5,
  "mAmp": 1, "mRate": 1,
  "ripple": { "freq": 22, "rate": 6, "amp": 0.05 },
  "flash": 0, "offset": [0, 0]
}
```

| 字段 | 含义 | 范围 |
|---|---|---|
| mode | 运动模式 | vortex / ripple / splash / wave / tide / rays / kaleido |
| c1 / c2 / c3 | 主色 / 亮色 / 暗色 | 十六进制颜色 |
| contrast | 对比度 | 0.2 – 5 |
| spinAmount | 旋转量 | 0 – 2 |
| speed | 速度 | 0 – 2 |
| pixelSizeFac | 像素细腻度（越大越细） | 100 – 4000 |
| spinEase | 旋转缓动 | 0 – 2 |
| mAmp / mRate | 运动强度 / 运动速率 | 0 – 3 |
| ripple.freq / rate / amp | 涟漪频率 / 速率 / 幅度 | 2–60 / 0–20 / 0–0.2 |
| flash | 中心闪光 | 0 – 1 |
| offset | 中心偏移 [x, y] | −0.4 – 0.4 |

## 出处 Origin

这个编辑器诞生于独立游戏《国王棋 CHESS OF KING》（哥特教堂风国际象棋肉鸽）的开发过程：
主菜单背景的调参台用顺手了，干脆做成开源工具分享出来。开发日志在 Bilibili 持续更新。

Born during the development of the indie game *Chess of King* — the main-menu background
tuner turned out handy enough to share. Dev logs on Bilibili.

## 免责声明 Disclaimer

本项目为非官方的风格致敬作品，与 LocalThunk、Playstack 无任何关联。
“Balatro”是 Playstack 的注册商标。本项目的着色器为原创实现，仅借鉴同类流体旋涡的
通用图形技法；全部预设名称与配色均为自创。

Unofficial fan-made tool, not affiliated with LocalThunk or Playstack. "Balatro" is a
registered trademark of Playstack. The shader is an original implementation using common
domain-warping techniques; all presets are original creations.

## License

MIT，见 [LICENSE](LICENSE)。可自由用于个人与商业项目，保留版权声明即可。
