# 稳定币理财收益计算器

Biteye 出品。对比 7 家交易所稳定币理财产品的阶梯利率，输入本金和期限，算出只存一家或组合存入的最高收益。

整个网站只有 `index.html` 一个文件，计算都在读者浏览器里完成，不需要服务器。

## 发布（GitHub Pages）

1. 把 `index.html` 和本文件放在仓库根目录。
2. 仓库 Settings → Pages → Source 选 “Deploy from a branch”，分支 `main`，目录 `/ (root)`，保存。
3. 一两分钟后可通过 `https://<组织名>.github.io/<仓库名>/` 访问。

## 绑定 Biteye 子域名

1. Settings → Pages → Custom domain 填入子域名（例如 `yield.<Biteye 域名>`），保存，生效后勾选 Enforce HTTPS。
2. 在 Biteye 域名的 DNS 后台添加记录：`CNAME`，名称 `yield`，值 `<组织名>.github.io`。

## 更新数据

产品利率写在 `index.html` 里的 `const P = [ ... ]`，每行一款产品。改完重新提交即可，GitHub Pages 会自动更新。当前数据抓取于 2026-11-03。
