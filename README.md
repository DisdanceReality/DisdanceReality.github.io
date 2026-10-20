# 王绍宇 个人学术主页

纯静态页面（`index.html` + `assets/`），不依赖任何构建工具，可直接部署到 GitHub Pages。

## 目录

```
index.html          页面本体（内容、样式、脚本都在这一个文件里）
assets/img/         头像与论文插图
.nojekyll           让 GitHub Pages 原样发布文件
```

## 部署到 GitHub Pages

1. 注册 GitHub 账号，新建一个公开仓库，仓库名必须是 `你的用户名.github.io`。
2. 把本目录下的全部文件（包括 `.nojekyll`）上传到仓库根目录：
   - 网页方式：仓库页面 → Add file → Upload files，把文件拖进去后提交；
   - 命令行方式：
     ```bash
     cd academic-homepage
     git init && git add . && git commit -m "init homepage"
     git branch -M main
     git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
     git push -u origin main
     ```
3. 仓库 Settings → Pages，Source 选 `Deploy from a branch`，分支选 `main` / `(root)`。
4. 等 1～2 分钟后访问 `https://你的用户名.github.io`。

## 常见修改

- **加简历 PDF**：把去掉电话号码的简历放到 `assets/cv.pdf`，再在 `index.html` 里取消对应按钮的注释。
- **加 GitHub / Google Scholar 链接**：在 `index.html` 顶部个人信息处取消注释并替换链接。
- **论文状态变化**（如录用）：修改对应论文卡片里的 `badge status` 文字和"近期动态"列表。
- **本地预览**：直接双击 `index.html` 用浏览器打开即可。
