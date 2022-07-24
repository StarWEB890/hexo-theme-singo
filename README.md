# Hexo Theme SinGO
[![OSCS Status](https://www.oscs1024.com/platform/badge/StarWEB890/hexo-theme-singo.svg?size=small)](https://www.oscs1024.com/project/StarWEB890/hexo-theme-singo?ref=badge_small)   [![MIT](https://img.shields.io/badge/license-MIT-brightgreen)](https://github.com/StarWEB890/hexo-theme-singo/blob/master/LICENSE)

一个基于[hexo-theme-material-flow](https://github.com/stkevintan/hexo-theme-material-flow)~~重做~~修改的主题

（2022-07-19：[hexo-theme-shana](https://github.com/ShanaMaid/hexo-theme-shana/)原主题手机访问有BUG，所以换成了[hexo-theme-material-flow](https://github.com/stkevintan/hexo-theme-material-flow)）
## 与hexo-theme-shana相比：
1.添加背景（由[LoliAPI](https://www.loliapi.com/)提供的 随机调用二次元图片API）

2.由于原先的主题没有pjax，所以我添加了pjax

3.保留了之前SinGO主题的风格

4.添加~~Waline~~、Gitalk、Twikoo、[Discuss](https://discuss.js.org/)评论
``` bash
2022-07-20：由于Waline手机访问有BUG，所以将其去掉，如果有解决方法，欢迎跟我PR！
```

5.添加网页在线聊天系统

6.添加不蒜子计数器

7.添加网站天气预报

8.添加网页播放音乐

9.添加萌ICP备案（PS：仅提供萌站长交流！不是真正的中国备案！）

## 效果展示
![主页](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_QhHdPzbFE1.4ll82e7jsb20.webp)
![主页+天气功能](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_SujqMwqThI.odmjaisoyw0.webp)
![归档](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_JWt1Gma2UT.615yjwaqoao0.webp)
![新功能：Discuss评论](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_C1uChRAFLo.8zo13bmp94g.webp)
## 使用教程
1.安装主题
``` bash
# 普通线路
git clone https://github.com/StarWEB890/hexo-theme-singo.git themes/singo
# FastGit加速线路
git clone https://hub.fastgit.xyz/StarWEB890/hexo-theme-singo.git themes/singo
# github.91chi.fun加速线路
git clone https://github.91chi.fun/https://github.com/StarWEB890/hexo-theme-singo.git themes/singo
```
2.安装插件
``` bash
# 普通线路
npm i -S hexo-generator-search hexo-generator-feed hexo-renderer-less hexo-autoprefixer hexo-generator-json-content
# cnpm加速线路（需要安装cnpm）
# 安装cnpm：npm install -g cnpm --registry=https://registry.npmmirror.com
cnpm i -S hexo-generator-search hexo-generator-feed hexo-renderer-less hexo-autoprefixer hexo-generator-json-content
```
3.同时将themes/singo/_source/的tags、categories和search文件夹拷贝到hexo根目录下的source文件夹下

4.修改根目录下的_config.yml

①修改theme为singo
``` yml
theme: singo
```
②在末尾添加：
``` yml
plugins: hexo-generate-feed

search:
  path: search.xml
  field: post

autoprefixer:
  exclude:
    - '*.min.css'
  # remove: false # prevent autoprefixer remove page-break-inside
  # browsers:
  #   - 'last 2 versions'
  #   - '> 5%'

# Generator json content
jsonContent:
  meta: false
  keywords: false
  pages:
    title: true
    slug: false
    date: false
    updated: false
    comments: false
    path: false
    link: false
    permalink: true
    excerpt: false
    keywords: false
    text: true
    raw: false
    content: false
  posts:
    title: true
    slug: false
    date: false
    updated: false
    comments: false
    path: false
    link: false
    permalink: true
    excerpt: false
    keywords: false
    text: true
    raw: false
    content: false
    categories: false
    tags: false

feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
```
④ 将`themes/singo/_source/`的`links`文件夹拷贝到hexo根目录下的`source`文件夹下
### 更新
``` bash
cd themes/singo
git pull origin master
``` 
## 更新日志
[点我查看](https://www.xsnetw.cf/update/) or [加入Q群：623816093](https://jq.qq.com/?_wv=1027&k=moLMRjwC)