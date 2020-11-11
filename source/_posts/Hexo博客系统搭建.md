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
new_post_name 新文章的文件名称， 默认 :title.md
default_layout   预设布局，默认post
auto_spacing  在中文和英文之间加入空格，默认false
titlecase     把标题转换为title case，默认false
extrnal_link  在新标签中打开链接，默认true
extrnal_link.enable 在新标签中打开链接, 默认true
extrnal_link.exclude  需要排除的域名。主域名和子域名如www需要分别配置，默认[]
filename_case 把文件名称转换为(1)小写或(2)大写， 默认0
render_drafts 显示草稿，默认false
post_asset_folder 启动Asset文件夹，默认false
relative_link   把链接改为与根目录的相对地址，默认false
future      显示未来的文章，默认true
highlight   代码块设置
prismjs     代码块的设置
```

**分类&标签 Category & Tags**
```
default_category 默认分类，默认uncategoryized
category_map 分类别名
tag_map      标签别名
```

**日期/时间 Date/Time**
```
date_format  日期格式  YYYY-MM-DD
time_format  时间格式  HH:mm:ss
updated_option 当Front Matter中没有指定update时updated的取值，默认mtime文件的最后修改时间
```

**分页Pagination**
```
per_page 每页显示的文章量(0 表示关闭分页)，默认10
pagination_dir 分页目录，默认page
```

**扩展 Extensions**
```
theme  当前主题名称，值为false时禁用主题
theme_config 主题的配置文件, 这里放置的配置会覆盖主题目录下_config.yml中的配置
deploy  部署部分的设置
meta_generator Meta generator标签。值为false时hexo不会在头部插入该标签
```

**包括或不包括目录和文件**
```
include 将包括的文件和目录，会复制到source目录下 
exclude 忽略文件和目录
ignore  忽略文件或目录
```