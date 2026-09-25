# 个人主页

基于 [academic-homepage-template](https://github.com/w-r-s/academic-homepage-template) 改造的中文个人主页，纯静态站点，无需构建工具。

**现在页面上所有 `【】` 包起来的内容都是占位符，需要你自己填。** 完整的填写说明见 **[填写指南.md](填写指南.md)**。

## 本地预览

直接双击 `index.html` 即可，或者起一个本地服务器：

```bash
python -m http.server 8080 --bind 127.0.0.1
```

然后打开 <http://127.0.0.1:8080/>。

## 文件结构

```
.
├── index.html          # 页面全部内容（文字、结构、脚本都在这一个文件里）
├── stylesheet.css      # 样式
├── 填写指南.md          # 占位符填写 + 部署说明
├── images/
│   ├── template/       # 头像、机构 logo
│   ├── paper/          # 论文配图
│   ├── experience/     # 页脚背景图（多分辨率）
│   └── icon/           # 鼠标指针、工具图标
└── .nojekyll           # 让 GitHub Pages 跳过 Jekyll 处理
```

## 页面区块

| 区块 | 锚点 | 说明 |
|---|---|---|
| 关于 | `#about` | 姓名、简介、联系方式、头像 |
| 最新动态 | `#news` | 时间线式短动态 |
| 论文发表 | `#publications` | 带研究兴趣标签筛选 |
| 教育与工作经历 | `#experience` | |
| 项目 | `#projects` | 3D 旋转标签云，数据在 JS 数组里 |
| 学术服务与教学 | `#service` | |
| 荣誉与奖励 | `#awards` | |

窗口宽度大于 1500px 时，右侧会显示章节快捷导航。

## 部署

推到 GitHub 后在仓库 **Settings → Pages** 里把 Source 设为 `Deploy from a branch`，分支选 `main`、目录选 `/ (root)`。

## 说明

原模板的示例内容（虚构人物 Alex Morgan 及其论文、项目、奖项）已全部替换为中文占位符。
原始英文模板见 [academic-homepage-template](https://github.com/w-r-s/academic-homepage-template)。
