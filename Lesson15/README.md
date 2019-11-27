列表渲染
=========

## 知识点

* v-for

### v-for

循环数组元素，整理内容显示到页面上。

~~~html
<div id="myApp">
    <ul>
        <li v-for="(game, index) in games">({{index}}) {{game.title}} / 售价：{{game.price}}元</li>
    </ul>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            games: [
                {title:"勇者斗恶龙",price:500},
                {title:"库跑卡丁车",price:400},
                {title:"马里奥世界",price:550},
            ]
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
