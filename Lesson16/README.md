JS对象迭代
==========

## 知识点

* v-for

### v-for

循环JS对象，把对象内容循环显示到页面上。

~~~html
<div id="myApp">
    <h1>JS对象迭代</h1>
    <div v-for="(value, key) in mygame">
        {{ key }} : {{ value }}
    </div>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            mygame: {
                title: "乌贼娘2代",
                price: 350,
                pubdate: "2017年夏季",
                category: "射击",
                agerange: "全年龄",
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
