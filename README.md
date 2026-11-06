# dnd-legendary-npc-archive

DND经典传奇人物档案集：面向地下城主的中文静态资料站，收录 13 位角色及对应肖像，按形象层、灵魂层、演出与边界的三层九项结构整理。

采用羊皮纸、暗红与暗金配色的规则书风格，支持全文搜索、分组筛选、人物字号调整、肖像放大和打印。顶栏提供“官方 5e / AI”全站肖像切换，首次打开默认官方形象，后续保留读者的选择。无需后端、数据库、构建工具或外部 CDN。

## 打开与部署

- 本地预览：克隆或下载本仓库后，直接用 Chrome 或 Edge 打开 `index.html`。
- 网站发布：将 `index.html`、`assets/` 及其所有子目录一起上传到静态网站托管平台。
- 仓库根目录就是网站根目录，首页文件为 `index.html`，无需安装依赖或执行构建命令。
- 所有资源均使用相对路径，支持域名根目录或子目录部署。请保持文件夹结构完整。
- 本包不依赖外部图片、在线字体或第三方 CDN；部署后通过站点自身提供资源。

## 文件结构

```text
index.html                  页面结构与入口
assets/css/archive.css      界面样式与响应式、打印样式
assets/css/fonts.css        中文字体声明和字符分区
assets/js/archive.js        搜索、目录、字号、肖像切换与放大等交互
assets/data/npcs.js          13 位角色的正文及分组数据
assets/images/*.webp        13 张 AI 肖像
assets/images/official/     13 张用户选定的官方肖像及来源文件清单
assets/images/parchment.svg 羊皮纸纹理
assets/fonts/*.ttf          离线中文字体子集
assets/fonts/OFL.txt        Noto Serif SC 字体许可证
LICENSE                     MIT 协议
```

## 后续修改

- 修改角色文案：编辑 `assets/data/npcs.js` 中对应角色的 `pillar`、`soul`、`acting` 等字段，注意保留 JavaScript 字符串和数组语法。搜索索引会在页面加载时自动更新。
- 修改配色、间距、排版：编辑 `assets/css/archive.css`。
- 替换 AI 肖像：替换对应的 WebP 文件，或调整角色数据中的 `image` 相对路径。
- 替换官方肖像：调整 `officialImage` 相对路径；`officialPosition` 控制 CSS 裁切焦点。两套肖像在首页、卡片、详情和放大预览中均采用 832:1216（13:19）画框。
- 字体按当前内容制作了子集；新增字符若未被子集收录，浏览器会使用系统衬线字体显示。
- 字号与肖像版本选择保存在读者自己的浏览器中，不需要服务器数据库；浏览器不允许存储时，仍可在当前页面正常切换。

## 肖像与字体

AI 肖像使用原始 832×1216 PNG 转为 WebP，保留原分辨率。伊尔明斯特使用已确认的 v1 肖像；其余角色沿用终稿肖像。

官方肖像采用用户在“官网人物肖像”目录中选定的 13 张文件，保留原始图片字节、透明度及分辨率。页面使用固定 13:19 画框和逐人设置的裁切焦点，不拉伸、不覆盖原图。来源文件名、SHA-256、分辨率与裁切焦点记录在 `assets/images/official/manifest.json`。这里的“官方 5e”是界面的版本标签，其中明斯克与布布沿用用户选择的 `Minsc_and_Boo_CLB_alt.webp`，不表示所有插画都出自同一本 5e 出版物。

单文件 HTML 内嵌两套图片；分体站点从本地 `assets/` 加载，两种形式均不请求外部图片服务器。

中文字体为 Noto Serif SC，按 SIL Open Font License 1.1 使用；完整许可证见 `assets/fonts/OFL.txt`。

## 许可与第三方权利

整理与创作：**且听沧海Cecil**。本站仓库：[Cecil727/dnd-legendary-npc-archive](https://github.com/Cecil727/dnd-legendary-npc-archive)。

档案文本结合官方设定与主流中文跑团社区解读进行文学再创作，供扮演参考，不应视为纯官方设定。

本项目的原创代码及可授权的原创文本采用 [MIT License](LICENSE)。AI 肖像均由 AI 生成，作者可处分的权利以 [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/deed.zh-hans) 开放；范围及说明见 [AI 肖像许可声明](AI-IMAGES-LICENSE.md)。角色、商标及其他第三方权利除外。

官方插画版权归 Wizards of the Coast 及相应权利人所有，使用遵循其[《粉丝内容政策》](https://company.wizards.com/en/legal/fancontentpolicy)及原始来源说明；官方插画不适用本项目的 MIT 或 CC0 声明。Dungeons & Dragons、D&D 及相关角色、世界设定和商标的权利归各自权利人所有。本作是依《粉丝内容政策》发布的非官方粉丝内容，未经威世智批准或认可。部分素材版权归 Wizards of the Coast LLC 所有。© Wizards of the Coast LLC。

Noto Serif SC 字体继续遵循其 SIL Open Font License 1.1，详见 [字体许可证](assets/fonts/OFL.txt)。
