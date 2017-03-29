# A simply Pagination Plugin with Bootstrap

This is an extension script to jQuery Datatables.  It allows you to override the default pager for one with a textbox for entering page numbers.  It also implements a bootstrap highlight and glyphicons.  It is customizable and intuitive.

![Screenshot 1](https://raw.github.com/chadkuehn/bootstrapPager/master/asset/screenshot1.png)

![Screenshot 2](https://raw.github.com/chadkuehn/bootstrapPager/master/asset/screenshot2.png)

## Dependencies
 - [jQuery](https://github.com/jquery/jquery) (v1.64 or newer)
 - [jQuery DataTables](https://github.com/DataTables/DataTables) (v1.9.0 or newer)
 - [Twitter Bootstrap](https://github.com/twbs/bootstrap) (v3.0 or newer)

## Usage
Download the [archive](https://github.com/chadkuehn/BootstrapPager/releases/latest) or install the [nuget](https://www.nuget.org/packages/DatatablePaginateBootstrap/).

Add the script to the page after the dependencies:

```html
<script type="text/javascript" src="~/Scripts/bootstrapPager.min.js"></script>
```

**BASIC:**  
In your dataTable declaration select this plugin:
```javascript
$('#tbl').DataTable({
    pagingType: "bootstrapPager",
    ...
});
```
It’s as easy as that! 


**ADVANCED:**  
If you want to adjust some settings add the `pagerSettings` object:
```javascript
$('#tbl').DataTable({
    pagingType: "bootstrapPager",
    pagerSettings: {
        textboxWidth: 70,
        firstIcon: "",
        previousIcon: "glyphicon glyphicon-arrow-left",
        nextIcon: "glyphicon glyphicon-arrow-right",
        lastIcon: "",
        searchOnEnter: true,
        language: "Page ~ of ~ pages"
    },
    ...
});
```
The above settings would enlarge the textbox, change the icons from chevrons to arrows, remove the first and last buttons, and make it so searching requires an ENTER press.

If you are a FontAwesome fan simply reference the library and use those classes instead:

```javascript
$('#tbl').DataTable({
    pagingType: "bootstrapPager",
    pagerSettings: {
       firstIcon: "fa fa-angle-double-left fa-2x",
       previousIcon: "fa fa-angle-left fa-2x",
       nextIcon: "fa fa-angle-right fa-2x",
       lastIcon: "fa  fa-angle-double-right fa-2x"
    },
    ...
});
```

## Features
 - Uses glyphicons for image buttons (a font built into bootstrap)
 - Intuitive navigation images
 - Properly handles  ALL (or -1) as a Length
 - Hides pager if no records found (instead of showing Page 0 of 0)
 - Styles and icons can be overridden
 - Navigate on ENTER instead of every keystroke to conserve AJAX hits
 - Alter the language (i.e., use páginas instead of pages)
 - Set options easily through the pagerSettings object

## API
**PagerSettings:**

 - textboxWidth
 - firstIcon
 - previousIcon
 - nextIcon
 - lastIcon
 - searchOnEnter



## Support
Found a bug or have a feature request? [Open an issue](https://github.com/chadkuehn/BootstrapPager/issues/new ).  
 
## Author
**Chad Kuehn** ([@ChadillacMan](https://twitter.com/ChadillacMan))  
[http://chadkuehn.com](http://chadkuehn.com)

## Copyright & License
Copyright (c) 2014 Chad Kuehn  

BootstrapPager is available under the MIT license. See the [LICENSE file][7.1]
for more information.

[7.1]: ./LICENSE.txt