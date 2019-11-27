事件处理器
===========

## 知识点

* v-on:(event)/@(event)

### v-on:(event)

页面元素的事件绑定。（click,keyup,load等等）

~~~html
<div id="myApp">
    <h1>事件处理器</h1>
    <input id="txtName" v-on:keyup="txtKeyup($event)">
    <button id="btnOK" v-on:click="btnClick($event)">OK</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {},
        methods: {
            txtKeyup: function(event){
                this.debugLog(event);
            },
            btnClick: function(event){
                this.debugLog(event);
            },
            debugLog:function(event){
                console.log(
                    event.srcElement.tagName, 
                    event.srcElement.id, 
                    event.srcElement.innerHTML, 
                    event.key?event.key:""
                );
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
