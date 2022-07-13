# Hexo Theme SinGO
[![OSCS Status](https://www.oscs1024.com/platform/badge/StarWEB890/hexo-theme-singo.svg?size=small)](https://www.oscs1024.com/project/StarWEB890/hexo-theme-singo?ref=badge_small)   [![MIT](https://img.shields.io/badge/license-MIT-brightgreen)](https://github.com/StarWEB890/hexo-theme-singo/blob/master/LICENSE)

一款基于[hexo-theme-shana](https://github.com/ShanaMaid/hexo-theme-shana/)修改 ~~（重做）~~ 的主题
## 与hexo-theme-shana相比：
1.由于原主题是原作者为庆贺夏娜酱2016年加冕萌王而制作的，而且animation也很多，低配手机在移动端访问的时候可能会出现卡顿，所以删去GalMenu和bganimation（如果想要的话我可以加回来）等内容，背景换成由[LoliAPI](https://www.loliapi.com/)提供的 随机调用二次元图片API

~~（毕竟二次元内容越来越丰富，不可能只有夏娜酱一个吧，但她也有可能成为时代的眼泪了……）~~

2.由于原先的主题没有pjax，所以我添加了pjax，把和pjax冲突的wow删去了

~~我现在怀疑我不是修改这个主题，而是把整个主题推翻重做了。。。。~~

3.删去原先的搜索功能，改用本地搜索

4.删去友言、Disqus评论，新增Waline、Gitalk评论（为啥删去disqus？我看原主题的_config.yml没有disqus这个选项，就把它删去了。毕竟disqus在国内被墙了。。。）

5.添加网页在线聊天系统

6.添加不蒜子计数器（我一直都喜欢用这个）

7.添加网站天气预报

8.添加网页播放音乐

9.添加萌ICP备案（PS：仅提供萌站长交流！不是真正的中国备案！）

10.添加顶部栏

11.去掉网页鼠标指针

## 效果展示
![主页](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_wmU4dIlJjH.591jwk3e7zk0.webp)
![主页+Chatra+和风天气](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_yvUcsKcGpB.1tj45k0kcn9c.webp)
![主页+心知天气](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_1kdQdEPMdm.1hz08g118p4w.webp)
![归档页+APlayer](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_P051Qkvd2c.48w206dorua0.webp)
![分类页](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_XffYi8c6o2.3tozmmqph3o0.webp)
![标签页](https://cdn.staticaly.com/gh/StarWEB890/TuChuang@master/images/msedge_6gYkIb2anS.395bt75ieou0.webp)

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
npm install hexo-generator-feed --save
npm install hexo-generator-search --save
# cnpm加速线路（需要安装cnpm）
# 安装cnpm：npm install -g cnpm --registry=https://registry.npmmirror.com
cnpm install hexo-generator-feed --save
cnpm install hexo-generator-search --save
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
```

### 更新
``` bash
cd themes/singo
git pull origin master
``` 
## 启用数学公式

1.卸载`hexo-renderer-marked`

``` bash
npm uninstall hexo-renderer-marked --save
```
2.安装`hexo-renderer-markdown-it-plus`
``` bash
# 普通线路
npm install hexo-renderer-markdown-it-plus --save
# cnpm加速线路（需要安装cnpm）
cnpm install hexo-renderer-markdown-it-plus --save
```
3.在需要启用数学公式的博客的head添加math: true

4.编辑根目录下的_config.yml,在最后添加：

``` yaml
markdown_it_plus:
  highlight: true
  html: true
  xhtmlOut: true
  breaks: true
  langPrefix:
  linkify: true
  typographer:
  quotes: “”‘’
  pre_class: highlight
```

## 自定义代码高亮

编辑`hexo-theme-shana\source\css_partial\highlight.styl`

![](https://user-images.githubusercontent.com/20333903/28317264-c8a80a28-6bf8-11e7-88f9-f1ef542f5118.png)

## 更新日志
[点我查看](https://github.com/StarWEB890/hexo-theme-singo/blob/master/UPDATE.md) or [加入Q群：623816093](https://jq.qq.com/?_wv=1027&k=moLMRjwC)
