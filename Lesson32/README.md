组件：组合slot
==============

## 知识点

* slot命名

### slot命名

在子组件中通过为多个slot进行命名,来接受父组件的不同内容的数据。

## 综合例

~~~html
<div id="myApp">
    <nba-all-stars c="奥尼尔" pf="加内特">
        <span slot="sf">皮尔斯</span>
        <span slot="sg">雷阿伦</span>
        <span slot="pg">隆多</span>
    </nba-all-stars>
</div>
<script>
    Vue.component('nba-all-stars', {
        props: ['c', 'pf'],
        template: '<div>'
            + '<div>中锋：{{c}}</div>'
            + '<div>大前：{{pf}}</div>'
            + '<div>小前：<slot name="sf"></slot></div>'
            + '<div>分卫：<slot name="sg"></slot></div>'
            + '<div>控卫：<slot name="pg"></slot></div>'
            + '</div>',
    });
    var myApp = new Vue({
        el: '#myApp',
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
