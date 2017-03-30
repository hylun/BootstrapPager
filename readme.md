# 一个精巧的Bootstrap分页插件

这是一个javascript实现的Bootstrap分页插件，非常精细小巧，您不需要依赖任何第三方类库，只需要通过简单的引用调用，即可实现动态显示Bootstrap分页组件。

![样式一](./asset/screenshot1.png)

![样式二](./asset/screenshot2.png)

## 样式依赖
 - [Twitter Bootstrap](http://getbootstrap.com) (v3.0 or newer)

## 用法
下载[附件](https://github.com/hylun/BootstrapPager/releases/latest).

将dist/bootstrapPager.js文件拷贝至您项目的目录下，比如js目录，
在页面中添加此js的引用：

```html
<script type="text/javascript" src="~/js/bootstrapPager.js"></script>
```

**基本用法**  
```javascript
document.write(Pager({
    totalCount:150 //总条数为150
}));
```
就是这么简单！ 


**高级用法**  
```javascript
document.write(Pager({
    totalCount:150, //总条数为150
    pageSize:6,    //每页显示6条内容，默认10
    buttonSize:6,   //显示6个按钮，默认10
    pageParam:'p',   //页码的参数名为'p'，默认为'page'
    className:'pagination',    //分页的样式
    prevButton:'上一页',       //上一页按钮
    nextButton:'下一页',       //下一页按钮
    firstButton:'首页',      //第一页按钮
    lastButton:'末页',       //最后一页按钮
}));
```

另外可以使用内置方法:

```javascript
document.write('url中page参数值为：'+Pager.getParam('page'));
document.write('替换Url中page参数值为3得到的地址：'+Pager.replaceUrl('page',3));
```


## API
```javascript
/**
*获取分页html字符串，用于显示分页
*@Param options json对象，属性有:
*       totalCount       总条数
*       pageSize         每页显示内容条数，默认10
*       buttonSize       显示按钮的个数，默认10
*       pageParam        页码参数名，默认为'page'
*       className        分页的样式，默认为'pagination'
*       prevButton       上一页按钮，默认<<
*       nextButton       下一页按钮，默认>>
*       firstButton      第一页按钮，默认不显示
*       lastButton       最后一页按钮，默认不显示
**/
function Pager(options);

/**
*获取url参数
*@Parame name 需要获取的参数的名称
**/
function Pager.getParam(name);

/**
*替换urlm某参数的值
*@Parame name 需要替换的参数的名称
*@Parame name 需要替换的参数的值
**/
function Pager.replaceUrl(name,value);

```

## 作者
**He Yuanlun**  [Blog](https://my.oschina.net/alun)

## Copyright & License
Copyright (c) 2017 He Yuanlun  

BootstrapPager is available under the MIT license. See the [LICENSE file][7]
for more information.

[7]: ./LICENSE.txt


