# kankan.liveplayer
看看直播播放器说明

1.引用库：

```
<link href="http://misc.vod.news.cn/v/misc/webapp.css" rel="stylesheet" type="text/css"/>
<script type="text/javascript" src="http://js.kankan.xunlei.com/js/sbase.js"></script>
<script type="text/javascript" src="http://js.kankan.xunlei.com/player/mp4/live/liveplayer1.2.js"></script>

```

2.HTML:

```
<div class="wrap">
    <div class="video_box">
        <div class="player" id="player_container">
            <div id="_player" style="height: 100%; width: 100%;"></div>
        </div>
        <div class="errorbox" style="display:none;" id="errorDiv"></div>
        <div class="error" style="display:none;" id="playerError">
            <p id="playerErrorContent"></p>
        </div>
        <noscript>
            <div class="errortxt">
                <p>检测到环境不支持JavaScript，请打开浏览器的 JavaScript 支持，或者降低浏览器安全级别。</p>
            </div>
        </noscript>
    </div>
</div>

```

3.代码调用

```
var G_PLAYER_LIVE = kankan.require("kkPlayerLive");

/*方法一*/
G_PLAYER_LIVE.playByHtml5('http://tw06017.sandai.net:8000/hls/rtmpsrc.m3u8',playCallback);

/*方法二*/
G_PLAYER_LIVE.danmu = true；
G_PLAYER_LIVE.playByFlash('rtmp://tw06017.sandai.net:1936/myapp/rtmpsrc',playCallback);

/*方法三*/
G_PLAYER_LIVE.play({
  url:'rtmp://tw06017.sandai.net:1936/myapp/rtmpsrc'，
  danmu：true
},playCallback);

function playCallback(err){
    if(err){
        console.log(err);
    }
}
```
