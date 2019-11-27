条件与循环
==========

## 知识点

* v-if
* v-for

### v-if

条件判断式，根据表达式的真伪进行页面处理。

~~~html
<p v-if="seen">快看我！</p>
~~~

### v-for

处理数组循环，将数据循环显示到页面上。

~~~html
<ol>
  <li v-for="game in games">
    {{ game.title }}
  </li>
</ol>
~~~

## 综合例

~~~html
<div id="myApp">
    <h3>游戏列表</h3>
    <div v-if="seen">2017最新发卖</div>
    <ol>
        <li v-for="game in games">{{game.title}} / {{game.price}}元</li>
    </ol>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            seen: true,
            games: [
                {title:'勇者斗恶龙',price:400},
                {title:'超级马里奥',price:380},
                {title:'我的世界',price:99},
            ],
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
