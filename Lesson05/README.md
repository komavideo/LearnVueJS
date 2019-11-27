按钮事件
=========

## 知识点

* v-on

### v-on

为页面元素绑定各种事件。（keydown, keyup, click, dbclick, load, etd.）

~~~html
<div id="myApp">
    <p>您最喜欢的游戏是：{{mygame}}</p>
    <button v-on:click="btnClick('我的世界')">我的世界</button>
    <button v-on:click="btnClick('勇者斗恶龙')">勇者斗恶龙</button>
    <button v-on:click="btnClick('塞尔达传说')">塞尔达传说</button>
    <button @click="btnClick('魔界战记5')">魔界战记5</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            mygame: '超级马里奥'
        },
        methods: {
            btnClick: function(pname){
                this.mygame = pname;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
