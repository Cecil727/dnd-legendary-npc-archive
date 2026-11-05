# dnd-legendary-npc-archive

DND经典传奇人物档案集：面向地下城主的中文静态资料站，收录 13 位角色及对应肖像，按形象层、灵魂层、演出与边界的三层九项结构整理。

采用羊皮纸、暗红与暗金配色的规则书风格，支持全文搜索、分组筛选、人物字号调整、肖像放大和打印。无需后端、数据库、构建工具或外部 CDN。

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
assets/js/archive.js        搜索、目录、字号、肖像放大等交互
assets/data/npcs.js          13 位角色的正文及分组数据
assets/images/*.webp        13 张网页肖像
assets/images/parchment.svg 羊皮纸纹理
assets/fonts/*.ttf          离线中文字体子集
assets/fonts/OFL.txt        Noto Serif SC 字体许可证
LICENSE                     MIT 协议
```

## 后续修改

- 修改角色文案：编辑 `assets/data/npcs.js` 中对应角色的 `pillar`、`soul`、`acting` 等字段，注意保留 JavaScript 字符串和数组语法。搜索索引会在页面加载时自动更新。
- 修改配色、间距、排版：编辑 `assets/css/archive.css`。
- 替换肖像：替换对应的 WebP 文件，或调整角色数据中的 `image` 相对路径。
- 字体按当前内容制作了子集；新增字符若未被子集收录，浏览器会使用系统衬线字体显示。
- 字号保存在读者自己的浏览器中，不需要服务器数据库。

## 肖像与字体

肖像使用原始 832×1216 PNG 转为 WebP，保留原分辨率。伊尔明斯特使用已确认的 v1 肖像；其余角色沿用终稿肖像。原始 PNG 和离线单文件 HTML 无需随网站上传。

中文字体为 Noto Serif SC，按 SIL Open Font License 1.1 使用；完整许可证见 `assets/fonts/OFL.txt`。

## 许可与第三方权利

本项目的原创代码及可授权的原创内容采用 [MIT License](LICENSE)。

Noto Serif SC 字体继续遵循其 SIL Open Font License 1.1，详见 [字体许可证](assets/fonts/OFL.txt)。Dungeons & Dragons、D&D 及相关角色、世界设定和商标的权利归各自权利人所有；本项目的 MIT 协议不改变或授予这些第三方权利。本项目是非官方社区参考资料。
