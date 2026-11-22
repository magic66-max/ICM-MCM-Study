# ModelLab · 美赛数学建模学习网站

一个无需后端、可直接在浏览器中运行的中文 MCM/ICM 备赛学习网站。

## 功能

- 数学建模学习路线和进度记录
- 43 个常用模型的分类知识库、公式、案例及选型提示
- 英文建模论文写作教学与摘要练习
- LaTeX / Overleaf 实战教程
- 2004–2025 年获奖论文外部索引、精选案例及分析导读
- MCM/ICM A–F 六类题型指南与选题匹配
- Python 10 课实战课程（代码编辑、复制、下载及小测）
- 实战练习、模型选型助手、论文评分、四周计划与进度备份

> 注意：获奖论文索引为外部资源链接，并非对全部获奖作品的真实性、完整性或版权作出担保。标记为“分析导读”的部分不代表已经逐篇精读或权威评分。

## 快速开始

下载仓库并打开 `index.html` 即可使用，不需要安装依赖。若浏览器限制某些本地特性，也可以用任意静态文件服务器运行。

## 发布到 GitHub Pages（推荐：GitHub Actions）

1. 在 GitHub 创建公开仓库，例如 `ModelLab-MCM`。
2. **解压 ZIP 后上传文件夹里的全部内容**到仓库根目录（不要上传 ZIP 本身）；务必包含隐藏目录 `.github/workflows/deploy.yml`。
3. 进入 `Settings → Pages`，在 Build and deployment 中将 Source 设为 **GitHub Actions**。这是本项目提供的自动部署方式，无需点击分支模式的 Save。
4. 每次提交到 `main` 会自动触发部署；在仓库 `Actions` 查看工作流结果，成功后通过 Pages 页面给出的 URL 打开网站。
5. 如果 Pages 页面当前已经选择了 GitHub Actions，直接提交 `deploy.yml` 和网站文件即可；不需要选择右侧的静态 HTML 模板。

项目网站地址通常为 `https://<用户名>.github.io/<仓库名>/`。如使用 `magic66-max/ModelLab-MCM`，地址通常是 `https://magic66-max.github.io/ModelLab-MCM/`（需在部署成功后验证）。

也可改用 `Deploy from a branch`，选择 `main` / `/(root)`；此时不需要使用本项目的 Actions 工作流，建议只选一种部署方式。

## 项目结构

```text
.
├── .github/workflows/deploy.yml # 自动部署到 GitHub Pages
├── index.html             # 完整的前端网站
├── README.md              # 项目说明及部署方式
├── LICENSE                # MIT 代码许可证
├── CONTRIBUTING.md        # 贡献指南
├── .nojekyll              # GitHub Pages 静态文件配置
└── .gitignore
```

## 内容和版权说明

本项目中的原创网站代码以 MIT License 开源。对第三方文献、获奖论文、商标、题目及外部资源的权利不作任何授权。**请不要直接提交未经授权的获奖论文 PDF**；外部链接资源的版权属于各自权利人。使用前请核对最新的 COMAP 参赛要求与论文格式。

## 贡献

欢迎通过 Issue 反馈错误，通过 Pull Request 增加经过核实的模型教程、开放资源、论文点评和代码示例。见 [CONTRIBUTING.md](CONTRIBUTING.md)。


## 建模工作台（新增）

- **模型选型助手**：结合任务、数据条件和研究目标推荐候选方法与验证清单（启发式指导）。
- **论文精读评分卡**：六维学习评分与证据笔记，非官方评奖标准。
- **四周备赛计划**：12 项可打卡训练任务。
- **学习数据备份**：导出 JSON 并在其他浏览器恢复本地记录。

部署到 GitHub Pages 后无需后端服务器。所有进度数据保存在当前浏览器，不会自动同步到 GitHub。


## A–F 美赛题型指南（新增）

新增完整的 MCM/ICM 六题型介绍页面，包括官方题型定位、2026 年题目示例、适用模型、研究步骤、常见错误与选题适配问答。静态运行，不依赖后端。参考资料：<https://comap.org/contests/mcm-icm> 与 <https://contest.comap.com/undergraduate/contests/mcm/contests/2026/problems/index.html>。


## 🐍 Python 实战训练营（新增）

网站左侧 **Python 实战** 包含 10 节由浅入深的代码课程：环境配置、NumPy、Pandas、Matplotlib、回归、熵权 TOPSIS、K-means、线性规划、蒙特卡洛和物资分配综合案例。每节有完整可编辑示例、预期输出、扩展任务与小测，支持复制、导出 `.py`、浏览器本地学习进度与草稿保存。

注意：GitHub Pages 只托管静态网站，**网页内并不执行 Python**。请将代码复制到 [Google Colab](https://colab.research.google.com/) 或 Jupyter / 本地 Python 运行。需要的第三方库包括 `numpy pandas matplotlib scipy scikit-learn`；建议在项目独立环境中安装。代码中的数据属于教学模拟样本，不代表真实赛题数据。
