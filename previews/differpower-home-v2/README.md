# DifferPower — Home 全页动效演示 v2

本版为独立 HTML/CSS/JavaScript 完整 Home 页演示。保留上一版首屏文件；没有修改个人网站，没有连接 Framer、导入 Framer 工程或部署网站。

## 下载与预览

打开本目录的 `index.html`，使用 GitHub 的 **Download raw file** 下载，保存为 HTML 后用浏览器打开。所有图片、字体、CSS 和 JavaScript 均已内嵌，文件约 8 MB，无需安装依赖或启动服务。外部导航链接需要联网。

- 直接滚动体验全页。
- 住宅示意图中的编号及底部圆点可切换场景。
- D Series 亮点支持横向浏览、左右按钮、方向键与手机触摸滚动。
- One System 示意图右下角按钮可放大，按 Escape 关闭。
- 右下角控制用于暂停 / 继续和返回顶部；页脚可重新播放入场动画。

## Home 内容覆盖

| 原官网内容 | 本版展示 |
| --- | --- |
| 导航及品牌 Logo | 白色半透明固定导航，原有菜单文字，手机菜单 |
| Modern Clean Energy | 大标题、原副标题与原山景图片 |
| How Energy Flows in a DIFFER Home | 原住宅剖面图、One Box. One Energy System.、三个原场景说明 |
| Engineered for Real Life | 原产品特写，固定滚动展示 |
| 原产品亮点长图 | 5 张可横向浏览的卡片，覆盖原图 9 组亮点 |
| One System | 原文案与原 D1 9-in-1 示意图，支持放大 |
| A Smarter Way to Power Your Home | 原星空住宅图片、原副标题与按钮 |
| Power with Us | 原文案、Learn More、原泳池和安装场景图片 |
| Explore Solutions / Become a Partner | 双入口卡片 |
| Sustainability | 原森林图、原说明与链接 |
| Footer | Solutions、Products、Partners、Support、About 全部原菜单及 LinkedIn 入口 |

原来的三组轮播主题分散为独立叙事段落，让内容可直接随滚动浏览。产品亮点通过 SVG 视窗重新取景原图，未生成替代品牌图片；图内文字和数值来自官网原图。本演示不新增产品性能主张。

## 视觉与动效方向

参考 [Apple 首页](https://www.apple.com/) 和 [Apple 产品页](https://www.apple.com/iphone-18-pro/) 的排版层级、留白、产品近景和分段展示方式。品牌仍使用 DifferPower 的 Inter 字体、原始图片和英文文案，新增强调色为 #FF691E，整体以白色为主。

动效包括标题遮罩、画幅展开、两段短固定滚动、产品缩放、场景图视差、横向卡片及悬停交互。没有拦截滚轮或触摸滚动；不依赖动画 CDN、WebGL 或外部脚本。

## 兼容性与性能验证

Chromium 离线渲染与交互检查覆盖 1440×1000、768×1024、390×844、360×640：内容完整，无页面横向溢出，无外部资源请求，无 JavaScript 运行错误。已检查入场动画、场景控制、产品滚动变换、亮点轮播、放大弹窗、手机菜单、暂停 / 继续与重播。

尊重 prefers-reduced-motion，减少动态效果时取消固定滚动及视差。滚动监听为 passive，requestAnimationFrame 按需执行，不持续空转；只为视口附近的主要图片更新变换，页面进入后台时停止更新。

当前云端 Chromium 管理策略禁止 file://，自动验证使用同一份 HTML 内容进行断网渲染。文件不需要 fetch、ES Module、本地存储或后端 API。未在实体 iPhone 或 Safari 上实测。

## 源码与素材

完整 HTML 内的 CSS 和 JavaScript 保持可读，可继续修改。主要参数：

- CSS `:root`：颜色、导航和页面边距。
- `.hero` / `.display`：字体层级。
- `.home-scroll` / `.product-scroll`：固定滚动长度。
- JavaScript `render()`：图片缩放与视差。
- SVG `viewBox` / `clipPath`：原产品图取景。
- 媒体查询：手机布局。

所有品牌素材来自 [DifferPower 公开官网](https://www.differpower.com/) 及其 framerusercontent.com 静态资源。没有操作 Framer 编辑器。
