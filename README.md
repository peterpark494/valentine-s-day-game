# Valentine's Day Game

这是一个可直接部署到 Vercel 的静态站点项目。

## 当前已上线网址

- 生产地址：<https://valentine-s-day-game-9td8bjz5f-peterparks-projects-d1055745.vercel.app>
- 如果之后重新部署或改了项目名，最新地址请以 `Vercel Dashboard -> Project -> Domains` 为准。

## 项目结构

- `index.html`：站点入口页面。
- `vercel.json`：Vercel 部署配置（clean URL、无尾斜杠）。

## 本地预览

```bash
python3 -m http.server 4173
```

打开：<http://localhost:4173>

---

## 获取公网网址（推荐：Vercel 网页端，不用 CLI）

> 你可以在 1~2 分钟内拿到可公开访问的网址。

1. 打开 <https://vercel.com/new>
2. 选择你的 Git 仓库（若还没上传，请先 push 到 GitHub/GitLab/Bitbucket）。
3. Framework Preset 选 `Other`（静态站点）。
4. 保持默认 Build 设置，点击 **Deploy**。
5. 部署完成后，页面顶部会显示：
   - `https://<project-name>.vercel.app`
   - 这就是可直接分享的公网地址。

### 在哪里看“最终网址”

- Vercel Dashboard → 你的项目 → **Domains**
- 生产环境地址通常为：`https://<project-name>.vercel.app`
- 如果绑定了自定义域名，会在同页面一并显示。

---

## 可选：CLI 部署（在你本机执行）

```bash
npm i -g vercel
vercel login
vercel --prod
```

命令执行后，终端会输出生产地址（通常也是 `*.vercel.app`）。

---

## 说明

当前这个执行环境无法访问 npm registry 安装 `vercel` CLI，
所以这里不能直接替你“代发部署并返回 URL”；
但项目已具备可部署状态，你在 Vercel 网页端导入后即可立即生成公网地址。

---

## 常见问题：`fatal: not a git repository`

这个报错表示你当前终端目录不是一个 Git 仓库（当前目录或上级目录里没有 `.git`）。

可按下面步骤处理：

1. 先进入你真实的项目目录（确保能看到 `README.md`、`index.html`、`vercel.json`）：

   ```bash
   cd <你的项目路径>
   ```

2. 用下面命令确认是不是仓库目录：

   ```bash
   git status
   ```

   - 如果能看到分支和文件变更，说明目录正确。
   - 如果仍然报同样错误，请先克隆仓库：

   ```bash
   git clone https://github.com/<你的用户名>/<你的仓库名>.git
   cd <你的仓库名>
   git status
   ```

3. 再执行推送命令：

   ```bash
   git push -u origin work:main
   ```
