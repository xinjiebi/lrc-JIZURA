# lrc-JIZURA — 歌词动态视频制作工具

上传歌曲和歌词，在浏览器里一键生成动态歌词视频（文字PV），并导出 MP4。

**在线使用：<https://xinjiebi.github.io/lrc-JIZURA/>**（打开自动进入简体中文版）

本项目基于 [JIZURA](https://github.com/852wa/JIZURA)（MIT 许可证）定制，感谢原作者 852wa。

## 功能

- 输入歌词（支持 LRC 时间戳），自动组装成动态排版视频：860 个部件 × 27 种风格，按 `R` 键整体随机重新生成
- 加载音乐后自动检测 BPM，让画面切点对齐节拍；也支持手动打点同步
- 导出 MP4（含音频）、连号 PNG、透明 PNG、绿幕/黑幕合成素材，以及 After Effects 用的 JSON 构成数据
- 7 种画面比例（16:9 / 9:16 / 4:3 / 1:1 等），720p~4K，24/30/60fps
- 7 种界面语言（简中 / 繁中 / 日 / 英 / 韩 / 印尼 / 越南）
- 全部处理在浏览器本地完成，歌曲和歌词不上传任何服务器

## 使用要求

- 推荐 **Chrome / Edge** 浏览器（导出 MP4 依赖 WebCodecs API）；Safari 16.4+、Firefox 130+ 也可使用
- 字体经国内镜像加载；也可以在应用内直接上传本地字体文件使用

## 本定制版相对原版的改动

- 品牌改为 lrc-JIZURA，默认打开简体中文版（根路径自动跳转）
- 字体源从 Google Fonts 切换为 fonts.loli.net 国内镜像
- 站点地址与 canonical 链接指向本仓库

## 目录说明

| 路径 | 内容 |
|---|---|
| `index.html` | 根路径跳转页（→ 简体中文版） |
| `zh-hans/` | 简体中文版（单文件应用） |
| `zh-hant/` `en/` `ko/` `id/` `vi/` | 其他语言版本 |
| `src/` `app/` | 浏览器版源码 |
| `build.py` | 构建脚本：`python3 build.py` 重新生成全部语言版本 |
| `JIZURA_AE.jsx` `JIZURA_CEP.zip` | After Effects 面板（原版构建产物） |
| `ae/` `cep/` | AE 面板源码 |

## 许可证

MIT，详见 [LICENSE](LICENSE)。用本工具制作的视频权利归制作者所有；所使用歌词和歌曲的权利归各自权利人所有。
