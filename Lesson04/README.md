处理用户输入
============

## 知识点

* v-model

### v-model

为页面输入框进行数据邦定，例如：

+ input
+ select
+ textarea
+ components

### 使用例

~~~html
<div id="myApp">
    <p>您最喜欢的游戏是：{{mygame}}</p>
    <input v-model="mygame">
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            mygame: '超级马里奥'
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
