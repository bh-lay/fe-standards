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
2.两种合理引入`js`的方法

* (1)在head内使用动态创建script标签的方式引入js，实现异步加载

```
<head>
<script type="text/javascript">var s = document.createElement("script"), h = document.getElementsByTagName("head")[0];s.type = "text/javascript";s.async = true;s.src = "min.base.js";h.appendChild(s);</script>
</head>
```
* (2)在底部`</body>`前使用同步加载的方式

```
<script src="http://l.tbcdn.cn/apps/top/x/sdk.js?appkey=21555299"></script>
</body>
```

* (3)标签语义化；代码简洁化；必要的注释；适当考虑内容的重要程度来安排文档流的先后顺序
* (4)移动端站点极度追求简洁，比如导航代码通常一个容器内编写一系列a标签即可，不必再写ul、li什么的，如

```
<div class=”nav”>
<a href=”#”>首页</a>
<a href=”#”>关于我们</a>
</div>
```
* (5)允许代码缩进，但须以一个tab等于4个空格来设置
* (6)可见的内联标签禁止换行书写，避免多人合作内联或者内联块状标签间的空白带来的问题，如下面是不太合理的