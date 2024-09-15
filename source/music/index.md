---

title: 音乐收藏
date: 2020-08-24 18:24:04
aplayer: true
comments: false

---
<h2> 我的音乐收藏 </h2>  
<h4> 2016-04-27 创建</h4>  
<div id="music-page">
</div>
<script>
    var userId = "3778678";
    var userServer = "netease";
    var userType = "playlist";
</script>
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/aplayer@1.10.1/dist/APlayer.min.css">
<script src="https://cdn.jsdelivr.net/npm/aplayer@1.10.1/dist/APlayer.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/meting@2.0.1/dist/Meting.min.js"></script>

<script>
    const params = new URLSearchParams(window.location.search);
    var _param = {
         getCustomPlayList: function () {
            const musicPage = document.getElementById("music-page");
            const playlistType = params.get("type") || "playlist";
            if (params.get("id") && params.get("server")) {
                var id = params.get("id");
                var server = params.get("server");
                musicPage.innerHTML = `<meting-js listMaxHeight="1500px"id="${id}"server="${server}"type="${playlistType}"mutex="true"preload="auto"order="random"autoplay="true"></meting-js>`;
            } else {
                musicPage.innerHTML = `<meting-js listMaxHeight="1500px"id="${userId}"server="${userServer}"type="${userType}"mutex="true"preload="auto"order="random"autoplay=true></meting-js>`;
            }
        }
    };

    _param.getCustomPlayList();
    const vh = window.innerHeight * 1;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
    window.addEventListener('resize', () => {
        let vh = window.innerHeight * 1;
        document.documentElement.style.setProperty('--vh', `${vh}px`);
    });

</script>