# Sublime-APICloud-Snippet
APICloud提供的标准Sublime扩展插件，在Sublime中集成APICloud扩展模块的代码提示

触发代码片段的指令格式为： `模块名-方法名`，之后点击<kbd>Tab</kbd>键即可进行补全

所以使用的时候只要记得当前模块名和方法名，即可补全对应的代码

---
## 示例

**api-alert**

```js
api.alert({
    title: '${1:this}', 
    msg: ${2:this}
});
```

**api-confirm**
```js
api.confirm({
    title: '${1:title}',
    msg: '${2:msg}',
    buttons:['确定', '取消']
},function(ret,err){
    if(ret.buttonIndex == 1){
        api.alert({msg: '点击了确定'});
    }
});
```