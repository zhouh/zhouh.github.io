# 周浩教授个人主页

清华大学AIR研究院周浩教授的个人学术主页，基于Jekyll构建的静态网站。

## 项目结构

```
├── _config.yml          # Jekyll配置文件
├── _layouts/            # 页面布局模板
├── _includes/           # 可复用组件
├── _posts/              # 博客文章
├── _site/               # 构建输出目录
├── static/              # 静态资源（图片、CSS、JS）
├── files/               # 文档文件（CV、论文等）
├── index.html           # 主页
├── index_nat.html       # 非自回归翻译页面
├── chinese_intro.html   # 中文介绍页面
├── publications.html    # 论文列表页
├── blog.html           # 博客页面
├── students.html       # 学生页面
├── old_pub.html        # 旧版论文页面
├── rss.xml             # RSS订阅源
├── *.bib               # BibTeX文献数据
├── bibtex_js.js        # 文献展示JS库
├── Gemfile             # Ruby依赖管理
└── update.sh           # Git更新脚本
```

## 核心功能

- **个人介绍**: 学术背景、研究方向、联系方式
- **论文管理**: 基于BibTeX的论文列表，支持搜索和分类
- **项目展示**: 最新研究成果和项目链接
- **博客系统**: Jekyll博客功能，支持RSS
- **响应式设计**: Bootstrap框架，移动端适配
- **动态数据**: GitHub星数、引用数实时获取

## 本地运行

### 环境要求
- Ruby 3.0+
- Jekyll 4.3+

### 安装依赖
```bash
bundle install
```

### 启动开发服务器
```bash
# 基础启动
bundle exec jekyll serve

# 带实时重载（推荐）
bundle exec jekyll serve --livereload

# 指定端口
bundle exec jekyll serve --port 8080
```
访问 `http://localhost:4000`

### 构建静态文件
```bash
bundle exec jekyll build
```

## 发版方法

### Git更新
```bash
# 使用更新脚本
./update.sh

# 或手动操作
git add .
git commit -m 'Update'
git push origin master
```

### GitHub Pages部署
项目支持GitHub Pages自动部署，推送代码到main分支即可自动构建。


## 技术栈

- **静态生成**: Jekyll 4.3
- **前端框架**: Bootstrap 3.3
- **文献管理**: bibtex-js
- **部署**: GitHub Pages / 手动部署
- **分析**: Google Analytics

## 更新日志
- 页面加载速度优化：通过预加载在线资源、异步调用接口、优化图片格式等方法减少传输包大小、提升页面访问速度。

- 大文件转储：pdf转为github releases存储，需根据实际github项目仓库改写index.html中的在线链接信息。

- 样式文件加载方式优化：删除不需要和未引用的bootstrap、map等文件，转为CDN加载。

- 清理老项目残留：删除`/_posts`文件夹和`/static/blog_images`下的示例blog文件，删除老项目部署脚本`deploy.sh`。更新`rss.xml`中的berkeley和sangjin引用为正确的周浩教授信息，修改`_layouts/post.html`中的disqus配置（如果你需要使用评论功能，需要在Disqus上注册'haozhou-blog'这个shortname），更新`_config.yml`中的网站配置信息。

- 项目迁移到GitHub管理：编写`README.md`文档介绍项目，编辑`.gitignore`去除构建和缓存等不需要的信息.

- added in 2020: I have used the bibtex-js to manage my paper list, please refer to [bibtex-js](https://github.com/pcooksey/bibtex-js) and [lileicc](https://github.com/lileicc/lileicc.github.io) for more information.

- Source code for my [homepage](http://zhouh.github.io/), which is forked from [sangjinhan](https://github.com/sangjinhan/homepage).Many thanks to [sangjinhan](https://github.com/sangjinhan/homepage).

