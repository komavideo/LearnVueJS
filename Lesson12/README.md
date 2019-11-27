Class对象绑定
=============

## 知识点

* v-bind:class

### v-bind:class

为html标记绑定样式单class对象。

~~~html
<div id="myApp">
    <div :class="myClass">红色文本</div>
    <button @click="btnClick">改变class吧</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            myClass: {
                active: true,
                big: true,
            },
        },
        methods: {
            btnClick: function(){
                this.myClass.big = false;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
