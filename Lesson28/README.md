组件：传递变量
==============

## 知识点

* 为组件传递变量数据

### 组件的数据

制作可接受变量参数的组件。

## 综合例

~~~html
<div id="myApp">
    <div>请输入您的名字：<input v-model="myname"></div>
    <hr/>
    <say-hello :pname="myname" />
</div>
<script>
    Vue.component('say-hello', {
        props: ['pname'],
        template: '<div>你好，<strong>{{pname}}</strong>！</div>',
    });
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            myname: 'Koma'
        }
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
