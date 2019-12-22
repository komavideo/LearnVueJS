组件：事件传递
===============

## 知识点

* v-on
* $emit

### v-on

侦听组件事件，当组件触发事件后进行事件处理。

### $emit

触发事件，并将数据提交给事件侦听者。

## 综合例

~~~html
<div id="myApp">
    <h1>人生加法</h1>
    <add-method :a="6" :b="12" v-on:add_event="getAddResult"></add-method>
    <hr/>
    <h3>{{result}}</h3>
</div>
<script>
    Vue.component('add-method', {
        props: ['a', 'b'],
        template: '<div><button v-on:click="add">加吧</button></div>',
        methods: {
            add: function(){
                var value = 0;
                value = this.a + this.b;
                this.$emit('add_event', {
                    result:value
                });
            }
        },
    });
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            result: 0
        },
        methods: {
            getAddResult: function(pval){
                this.result = pval.result;
            }
        },
    });
</script>
~~~

## 源文件

https://github.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
