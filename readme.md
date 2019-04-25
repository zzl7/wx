
**1.ios中input执行focus方法后无法调起键盘的解决办法**
- 直接说我的解决办法吧，在点击的按钮上同时绑定touchstart方法和click方法，touchstart方法中执行input显示的命令，click中执行input.focus() 的命令，完美的解决，ios和Android都可以正常的唤起键盘。


**2.ios 滑不下来**
- 失去焦点的时候执行

```
setTimeout(function () {
    var scrollHeight =
        document.documentElement.scrollTop || document.body.scrollTop || 0;
    window.scrollTo(0, Math.max(scrollHeight - 1, 0));
}, 100);

```