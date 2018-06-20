# An exquisite Bootstrap Pagination lugin

This is a javascript implementation Bootstrap Pagination plugin, very fine small, you do not need to rely on any third-party library, only through a simple reference call, you can dynamically display Bootstrap paging components.

![Style one] (./asset/screenshot1.png)

![Style two] (./asset/screenshot2.png)

## style dependencies
 - [Twitter Bootstrap] (http://getbootstrap.com) (v3.0 or newer)

## usage
Download [attachments] (https://github.com/hylun/BootstrapPager/releases/latest).

Copy the dist/bootstrapPager.js file to your project directory, such as the js directory,
Add a reference to this js in the page:

```html
<script type="text/javascript" src="~/js/bootstrapPager.js"> </script>
```

** basic usage **
```javascript
Document.write (Pager ({
    TotalCount: 150 // total number of 150
}));
```
Its that simple!


** Advanced usage **
```javascript
Document.write (Pager ({
    TotalCount: 150,  // total number of 150
    PageSize: 6,      // Show 6 per page, default 10
    ButtonSize: 6,    // show 6 buttons, default 10
    PageParam: 'p',   // The page parameter is named 'p' and defaults is 'page'
    ClassName: 'pagination',// paged style
    PrevButton: 'prev',     // previous button
    NextButton: 'next',     // next page button
    firstButton:'first',     // first page button
    lastButton:'last',       // last page button
}));
```

You can also use the built-in method:

```javascript
Document.write ('url in the page parameter value:' + Pager.getParam ('page'));
Document.write ('replace Url in the page parameter value of 3 get the address:' + Pager.replaceUrl ('page', 3));
```


## API
```javascript
/**
* Get the paging html string for displaying paging
* @ Param options json objects, attributes are:
Total total number of total
* PageSize      shows the number of pages per page, the default 10
* ButtonSize    show the number of buttons, the default 10
* PageParam     page parameter name, default is 'page'
* ClassName     paging style, defaults to 'pagination'
* PrevButton    previous button, default <<
* NextButton    next page button, default >>
* firstButton   first page button, not displayed by default
* lastButton    last page button, not displayed by default
**/
function Pager (options);

/**
* Get the url parameter
* @ Parame name The name of the parameter to be obtained
**/
function Pager.getParam (name);

/**
* Replace urlm with a value for a parameter
* @ Parame name The name of the parameter that needs to be replaced
* @ Parame name The value of the parameter to be replaced
**/
function Pager.replaceUrl (name, value);

```

## Author
**Hylun** [blog](http://blog.csdn.net/heylun)

## Copyright & License
Copyright (c) 2017 He Yuanlun

BootstrapPager is available under the MIT license. See the [LICENSE file][7]
For more information.

[7]: ./LICENSE.txt