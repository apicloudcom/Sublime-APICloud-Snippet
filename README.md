# APICloud Snippets

APICloud提供的标准Sublime扩展插件，在Sublime中集成APICloud扩展模块的代码提示，封装了包含api对象的所有方法、Attribute、Event.

同时包含 db、fs、bMap、FNScanner、UIScrollPicture 等二十多个常用模块的语法补全。

触发代码片段的指令格式为： `模块名-方法名`，之后点击<kbd>Tab</kbd>键即可进行补全

所以使用的时候只要记得当前模块名和方法名，即可补全对应的代码

更多信息请查看[Sublime APICloud 插件的安装和使用说明](http://docs.apicloud.com/APICloud/sublime-apicloud-plugin)

# 使用示例
---
__api-alert__ <kbd>Tab</kbd>

```js
api.alert({
    title: '${1:this}', 
    msg: ${2:this}
});
```

__uiscrollpicture-open__ <kbd>Tab</kbd>
```js
uiscrollpicture.open({
    rect: {
        x: ${1:0},
        y: ${2:0},
        w: ${3:320},
        h: ${4:480}
    },
    data: {
        paths: ['${5:image_path1}', '${6:image_path2}', '${7:image_path3}'],
        captions: ['${8:title1}', '${9:title2}', '${10:title3}']
    },
    styles: {
        caption: {
            height: ${11:35},
            color: '${12:color}',
            size: ${13:13},
            bgColor: '${14:bg_color}',
            position: '${15:position}'
        },
        indicator: {
            align: '${16:align_mode}',
            color: '${17:color}',
            activeColor: '${18:active_color}'
        }
    },
    placeholderImg: '${19:placeholder_image_path}',
    contentMode: '${20:content_mode}',
    interval: ${21:3},
    loop: ${22:true},
    fixedOn: '',
    fixed: ${23:false}
}, function(ret, err){
     if(ret.status){
        if(ret.eventType == 'click'){
            //点击图片的操作
            alert(ret.index);
        }
     }
});
```