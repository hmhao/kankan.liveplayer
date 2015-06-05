# live.js

    var G_PLAYER_LIVE = kankan.require("kkPlayerLive");

---

## 索引

- [属性](#属性)
  - [ENGINE_FLASH](#engineflash)
  - [ENGINE_HTML5](#enginehtml5)
  - [url](#url)
  - [autoplay](#autoplay)
  - [danmu](#danmu)
  - [playerInit](#playerinit)
  - [playerInstance](#playerinstance)

- [方法](#方法)
  - [play](#play-opts-callback-)
  - [playByFlash](#playbyflash-url-callback-)
  - [playByHtml5](#playby5tml5-url-callback-)


## 属性

### ENGINE_FLASH
> 常量，表示使用flash引擎播放视频

---

### ENGINE_HTML5
> 常量，表示使用html5引擎播放视频

---

### url
> 视频地址

---

### autoplay
> 视频自动播放
> 对于android手机自带的浏览器，这属性不一定有效
> live.autoplay = true | false；默认值为true

---

### danmu
> 使用弹幕控件
> 该属性仅使用flash引擎播放视频时有效
> live.danmu= true | false；默认值为false

---

### playerInit
> 播放器初始化完成标志

---

### playerInstance
> 播放器实例
> 

---

## 方法

### play( opts, callback )
> 通用的播放方法
> 
> Example: 
> ```
> live.play({
>    url: 'http://example/myapp/rtmpsrc.m3u8'，/*必填*/
>    engine：live.ENGINE_HTML5,   /*可选，会根据url选择播放引擎*/
>    danmu：true，               /*可选*/
>    autoplay：false             /*可选*/
> }, function(err){});
> ```
> 

##### 参数: 
* __opts__ `Object` 播放相关的属性
* __callback__ `Function` 开始播放后的回调函数

---

### playByFlash( url, callback )
> 使用flash播放视频，实际调用了[play](#play-opts-callback)方法
> 
> Example: 
> ```
> live.playByFlash('rtmp://example/myapp/rtmpsrc', function(err){});
> ```
> 

##### 参数: 
* __url__ `Object` 播放地址
* __callback__ `Function` 开始播放后的回调函数

---

### playByHTML5( url, callback )
> 使用html5播放视频，实际调用了[play](#play-opts-callback)方法
> 
> Example: 
> ```
> live.playByHtml5('http://example/myapp/rtmpsrc.m3u8', function(err){});
> ```
> 

##### 参数: 
* __url__ `Object` 播放地址
* __callback__ `Function` 开始播放后的回调函数

---