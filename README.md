猎豹移动前端编码规范
==============


##一.文件相关

1. 文件名以英文为主，可以使用下划线(如active.html)，在后端开发前的html页面如果数量比较多，为了方便寻找，可以使用数字+中文的形式(直观并且可以自动排序)；压缩包以项目名+日期的形式
2. 一律使用utf-8编码
3. html、css、js发布到线上都需要压缩
4. 在追求高度优化的站点，需要对图片也进行无损压缩

##二.HTML相关

1. 统一使用html5的dtd申明，并且title要尽量靠前，keywords和description，一个比较合理的示例

```
<!doctype html>
<html>
<head>
<meta http-equiv=Content-Type content="text/html;charset=utf-8">
<title>金山毒霸 – 最好的免费杀毒软件</title>
<meta name="keywords" content="金山毒霸,金山毒霸 2012,金山毒霸 2012体验版,金山毒霸2012免费下载" />
<meta name="description" content="杀毒软件免费下载 2012之全新金山毒霸2012今天正式发布alpha版本，马上报名体验，先睹为快！" />

````