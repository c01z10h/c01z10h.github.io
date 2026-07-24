# 陈梓鸿 · 2026年作品集

工业 / 3D 设计师个人作品集详情页。
本仓库是可直接托管在 **GitHub Pages** 的静态站点。

## 站点结构

| 路径 | 说明 |
| --- | --- |
| `index.html` | 站点入口（GitHub Pages 根目录） |
| `work-detail-mockup_files/` | 静态资源：图片、视频、3D 模型（GLB）、Three.js 模块、Draco 解码器 |

- 在线字体：Google Fonts（DM Serif Display / Outfit / JetBrains Mono）
- 全部资源引用均为相对路径，无需任何后端，纯静态托管即可运行。

## 本地预览

> ⚠️ 站点使用 **ES Module + fetch** 加载 3D 模型，必须通过 HTTP 访问，
> 不能直接双击 `file://` 打开（浏览器会拦截模块与跨源请求）。

```bash
# 在项目根目录执行
python -m http.server 8010
# 浏览器打开 http://127.0.0.1:8010/
```

## 部署（GitHub Pages）

本仓库已配置好静态资源，按以下流程即可上线：

1. 在 GitHub 新建仓库（Public）。
2. 本地执行（替换 `USERNAME/REPO`）：
   ```bash
   git remote add origin https://github.com/USERNAME/REPO.git
   git branch -M main
   git push -u origin main
   ```
3. 仓库 **Settings → Pages → Build and deployment → Source: Deploy from a branch →
   Branch: `main` / Folder: `/(root)` → Save**。
4. 等待 1–2 分钟，访问 `https://USERNAME.github.io/REPO/`。

> 资源总量约 328 MB，全部单文件 < 100 MB，无需 Git LFS。
> 首次 push 体积较大，请耐心等待。

## 重新生成站点

源工程通过 `gen_mockup.py` 生成（见本地源工程，不在本仓库内）。
重新生成后，脚本会自动同步产出 `index.html`，直接提交即可更新线上站点。

---
© 陈梓鸿 · 工业设计 / 3D 可视化
© 2026 陈梓鸿，未经授权禁止商用/转载
