# FavHub 收藏管理

使用GitHub Issues管理收藏，并通过GitHub Pages展示的个人收藏网站。

## 主要功能

- 使用Issue录入新的收藏条目，通过特殊标识`[收藏]`进行区分
- 使用GitHub Action监听Issue变化，自动将收藏数据保存为JSON
- 使用GitHub Pages展示收藏内容，基于Tailwind CSS构建美观的界面
- 支持多标签筛选和搜索功能

## 条目字段

每个收藏条目包含以下字段：
- title: 收藏项的标题
- url: 收藏项的链接
- description: 收藏项的描述
- tags: 标签列表（支持多选）

## 如何使用

### 1. 添加新收藏

有两种方式添加新的收藏：

- 在网站上点击"添加新收藏"按钮，填写Issue模板
- 直接在GitHub仓库创建一个新Issue，标题必须包含`[收藏]`标识

填写表单时可以选择多个标签，也可以添加自定义标签。

### 2. 使用标签筛选

- 点击"选择标签"下拉菜单，可以勾选多个标签进行筛选
- 点击已选标签右侧的"×"可以移除该标签
- 点击"清除筛选"可以移除所有标签筛选
- 点击收藏项中的标签也可以快速添加到筛选条件

### 3. 管理收藏

- 关闭Issue会从收藏列表中移除该项目
- 编辑Issue会更新对应的收藏内容
- 添加标签可以增加新的标签

### 4. 部署说明

1. Fork本仓库
2. 启用GitHub Pages（Settings > Pages > Source选择main分支）
3. 等待GitHub Action自动构建并部署
4. 访问 `https://[你的用户名].github.io/[仓库名]` 查看站点

## 技术细节

- 前端：HTML + Tailwind CSS + 原生JavaScript
- 数据存储：GitHub Issues转换为JSON文件
- 自动化：GitHub Actions
- 部署：GitHub Pages

## 自定义

- 修改`.github/ISSUE_TEMPLATE/favorite.yml`可以自定义Issue模板和预设标签
- 修改`.github/scripts/sync-issues.js`中的`COMMON_TAGS`可以更改常用标签列表
- 修改`index.html`可以自定义界面外观

## 贡献

欢迎提交Pull Request或提出建议。

## 许可

MIT License