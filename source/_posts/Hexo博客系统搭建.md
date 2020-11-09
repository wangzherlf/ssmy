---
title: Hexo博客系统搭建
---

Hexo是一个快速、简洁且高效的博客框架

**Hexo的特点**
1. 超快速度 Node.js所带来的超快的生成速度
2. 支持Markdown 
3. 一键部署 一条命令可以部署到GitHub Page, Heroku或其他平台
4. 插件和可扩展性 与各种模板引擎(EJS, Nunjucks)和工具(Babel, PosCSS, Less/SaSS)轻易集成

**快速入门**
```
npm install hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
```
## 开始使用
### 创建项目
```
hexo init <folder>
cd <folder>
npm install
```
- `_config.yml` 网站的配置信息
- package.json  应用程序信息。 EJS, Styleus和Markdown render已默认安装
- scaffolds 模板文件夹. 新建文章时Hexo会根据scaffold来默认填充结构
- source 资源文件夹是存放用户资源的地方。除`_posts`文件夹外，以`_`开头的文件/文件夹及隐藏文件都会被忽略。Markdown和HTML文件会被解析并放到public文件夹，其他文件会被直接拷贝过去
- themes 主题文件夹

### 配置
**站点Site**
```
title      网站标题
subtitle   网站副标题
description 网站描述
keywords    关键词
author      作者
language    网站使用语言 zh-CN
timezone    网站时区 Asia/ShangHai
```

**网址URL**
```
url    网址，必须以http://或https://开头
root   网站根目录
permalink 文章的永久链接格式 :year/:month/:day/:title/
permalink_defaults 永久链接中各部分的默认值
pretty_urls  改写permalink值来美化URL
pertty_urls.trailing_index 是否在永久链接中保留尾部index.html
pertty_urls.trailing_html  是否在永久链接中保留尾部.html
```

**目录Directory**
```
source_dir 资源文件夹，用来存放文章，默认source
public_dir 公共文件夹，用来存放生成的站点文件，默认public
tag_dir    标签文件夹，默认tags
archive_dir 归档文件夹，默认archives
category_dir 分类文件夹，默认categories
code_dir   include code文件夹，默认downloads/code
i18n_dir   国际化i18n文件夹，默认:lang
skir_render 跳过指定文件的渲染。匹配到的文件夹将不做改动地复制到public目录中。如"mypage/**/*", "_posts/test.md"
```

**文章Writing**
```

```