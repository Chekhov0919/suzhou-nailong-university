# 苏州奶龙大学 🐲

> 一个纯静态的趣味跳转页：打开就是奶龙壁画背景的"苏州奶龙大学"首页，倒计时结束后自动前往 [苏州大学官网](https://www.suda.edu.cn/)。

已按 GitHub Pages 的部署要求组织好目录，**上传即可上线**。

---

## 一、目录结构

```
苏州奶龙大学/
├── index.html          # 主页面（背景 / 校名 / 倒计时跳转 / 免责声明）
├── 404.html            # 404 兜底页，自动回首页
├── assets/
│   ├── nailong.png     # 背景图（就是你给的那张"奶龙创世纪"）
│   └── favicon.svg     # 校徽风格图标
├── robots.txt          # 允许搜索引擎抓取 + 指向 sitemap
├── sitemap.xml         # 站点地图（提交给搜索引擎用）
├── .nojekyll           # 让 GitHub Pages 跳过 Jekyll 处理
└── README.md
```

**本地预览**：直接双击 `index.html` 就能看（不用装任何环境、不用起服务器）。

**想改跳转地址**：打开 `index.html`，搜索 `https://www.suda.edu.cn/`，共出现在 3 处（倒计时脚本里的 `TARGET`、按钮 `href`、页脚链接），一起改掉。

**想改倒计时秒数**：`index.html` 脚本里的 `var TOTAL = 6;`。
**想换背景图**：覆盖 `assets/nailong.png` 即可（建议 1600px 宽、1MB 以内，太大会拖慢首屏）。

---

## 二、部署到 GitHub Pages（约 3 分钟）

1. 在 GitHub 上新建一个仓库，比如 `suzhou-nailong-university`，**设为 Public**（私有仓库的 Pages 需要付费）。
2. 在本文件夹里打开终端，执行：

```bash
git init
git add .
git commit -m "feat: 苏州奶龙大学上线"
git branch -M main
git remote add origin https://github.com/你的用户名/suzhou-nailong-university.git
git push -u origin main
```

3. 打开仓库页面 → **Settings → Pages** → Source 选 `Deploy from a branch`，Branch 选 `main` + `/ (root)` → Save。
4. 等 1～2 分钟，访问 `https://你的用户名.github.io/suzhou-nailong-university/`。

> 想让网址更好看、也更好被搜索引擎收录？可以绑定自己的域名：买一个域名后在 Pages 里填 Custom domain（例如 `nailong.xxx.com`），并在仓库根目录放一个 `CNAME` 文件，内容只写那一行域名。

---

## 三、关于"搜『苏州奶龙大学』就能搜到"——说点实话

**能做的（已经帮你做完了）**

- 页面标题、`<h1>`、description、keywords 里都精确包含了「苏州奶龙大学」这个完整关键词；
- 有 `robots.txt`、`sitemap.xml`、规范链接（canonical）、结构化数据（JSON-LD），符合搜索引擎抓取习惯。

**不能保证的（这是关键，别被"上传就有人搜到"忽悠）**

1. **新站需要时间**：Google / Bing 通常几天到几周才开始收录，百度更慢，且排名不固定。搜索时要用完整词「苏州奶龙大学」，只搜"奶龙"基本轮不到你。
2. **百度对 `*.github.io` 收录极差**，github.io 在国内访问也不稳定。如果目标是让国内朋友在**百度**里搜到，最好：绑自己的域名 + 换国内可访问的托管（Cloudflare Pages / Vercel / 腾讯云静态托管等），再到[百度搜索资源平台](https://ziyuan.baidu.com/)提交站点。
3. **主动提交收录**（做完这个会快很多）：
   - [Google Search Console](https://search.google.com/search-console)：添加资源 → 用 HTML 标记验证（把给的那行 `<meta>` 贴到 `index.html` 的 `<head>` 里）→ 提交 `sitemap.xml`；
   - [Bing Webmaster Tools](https://www.bing.com/webmasters)：同上，Bing 对 GitHub Pages 友好，收录最快；
   - 百度搜索资源平台：适合有自己域名的情况。
4. **外链很重要**：把网址发到贴吧、微博、知乎、QQ 群、B 站简介里。搜索引擎顺着外链爬过来的概率，比干等它自己发现高得多（这招在玩梗站上尤其有效——有人搜、有人点、有人转发，排名自然会上去）。

---

## 四、顺手提醒两件事（不吓人，但值得知道）

- **奶龙形象有版权**（奶龙属于原创 IP，不是公共素材）。个人玩梗、非商业、不注册成自己商标，风险通常不大；但**别用来卖东西、别开赞赏收费、别投放广告**，被版权方找上就不是玩笑事了。想更稳妥，可以换成自己画的"黄色小奶龙风格"表情包。
- **"苏州大学"是学校名称，校徽/校名标识受保护**。所以这个页面刻意做成了"一看就是玩梗"的样子：**没有使用苏州大学的校徽和官方视觉，并且页眉页脚都写了"与苏州大学无隶属关系"的免责声明**。请保留这些声明，也不要把它包装成官方招生、报名、缴费入口——那性质就变了。
- 别用 `.com` 类看起来像官方的域名 + 诱导性文案，容易被投诉下架。

祝奶龙大学越办越好，招生顺利。
