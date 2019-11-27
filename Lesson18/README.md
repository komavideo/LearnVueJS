表单控件绑定
============

## 知识点

* v-model
* input[type="text"]

### v-model

为表单控件元素创建双向数据绑定。（将JS变量的值“快速”设定到控件上，然后将用户输入的内容“快速”设置回JS变量）

~~~html
<div id="myApp">
    <h1>表单控件绑定</h1>
    <input type="text" v-model="message" placeholder="来呀，编辑我吧！">
    <p>Message is: {{ message }}</p>
    <textarea v-model="message" placeholder="加入多行编辑" rows="8" cols="34"></textarea>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            message: "我爱马里奥",
        },
        methods: {
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
