组件：slot插槽
==============

## 知识点

* slot

### slot

slot是父组件与子组件的通讯方式，可以将父组件的内容显示在子组件当中。

## 综合例

~~~html
<div id="myApp">
    <say-to pname="koma">
        你的视频做的太差了。
    </say-to>
    <say-to pname="mike">
        你千万不要学koma。
    </say-to>
    <say-to pname="john">
        你教教他们两个吧。
    </say-to>
</div>
<script>
    Vue.component('say-to', {
        props: ['pname'],
        template: '<div>'
            + '你好，<strong>{{pname}}</strong>！'
            + '<slot></slot>'
            + '</div>',
    });
    var myApp = new Vue({
        el: '#myApp',
    });
</script>
~~~

## 源文件

https://github.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
