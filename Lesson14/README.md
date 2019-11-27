元素显示
=========

## 知识点

* v-show

### v-show

标记是否显示html元素。(注意：v-show设置的标记在html DOM中不会消失)

~~~html
<div id="myApp">
    <h1 v-show="result">任天堂新一代主机Switch</h1>
    <button @click="btnClick">考试成绩</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            result: true
        },
        methods: {
            btnClick: function(){
                this.result = !this.result;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
