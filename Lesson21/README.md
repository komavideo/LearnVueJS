表单下拉框
==========

## 知识点

* v-model
* select

### 表单下拉框绑定

~~~html
<div id="myApp">
    <h3>你最喜欢的NBA球星是：</h3>
    <select v-model="likedNBAStar" style="width:210px;">
        <option>科比</option>
        <option>詹姆斯</option>
        <option>哈登</option>
        <option>库里</option>
        <option>杜兰特</option>
    </select>

    <h3>我的全明星：</h3>
    <select v-model="likedNBAStars" multiple style="width:210px;height:210px;">
        <option>阿德托昆博</option>
        <option>怀特赛德</option>
        <option>阿尔德里奇</option>
        <option>戴维斯</option>
        <option>格里芬</option>
        <option>詹姆斯</option>
        <option>杜兰特</option>
        <option>巴特勒</option>
        <option>德罗赞</option>
        <option>哈登</option>
        <option>科比</option>
        <option>韦德</option>
        <option>伦纳德</option>
        <option>库里</option>
        <option>欧文</option>
        <option>保罗</option>
        <option>林树豪</option>
    </select>

    <h3>选择结果</h3>
    <p>我最最喜欢: {{ likedNBAStar }}</p>
    <p>我的全明星: {{ likedNBAStars }}</p>

</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            likedNBAStar: null,
            likedNBAStars: [],
        },
        methods: {
        },
    });
</script>
~~~

## 源文件

https://github.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
