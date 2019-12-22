Class绑定
==========

## 知识点

* v-bind:class

### v-bind:class

为html标记绑定样式单class属性。

~~~html
<div id="myApp">
    <div v-bind:class="{active:isActive}">红色文本1</div>
    <div :class="{active:isActive}">红色文本2</div>
    <button @click="btnClick">改变class吧</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            isActive: true,
        },
        methods: {
            btnClick: function(){
                this.isActive = false;
            },
        },
    });
</script>
~~~

## 源文件

https://github.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
