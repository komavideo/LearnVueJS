表单复选框
==========

## 知识点

* v-model
* input[type="checkbox"]

### 表单复选框绑定

~~~html
<div id="myApp">
    <h1>表单复选框</h1>
    <input type="checkbox" id="生化危机7" value="生化危机7" v-model="checkedGames">
    <label for="生化危机7">生化危机7</label>
    <input type="checkbox" id="模拟飞行" value="模拟飞行" v-model="checkedGames">
    <label for="模拟飞行">模拟飞行</label>
    <input type="checkbox" id="塞尔达传说" value="塞尔达传说" v-model="checkedGames">
    <label for="塞尔达传说">塞尔达传说</label>
    <br>
    <p>您选择的游戏是: {{ checkedGames }}</p>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            checkedGames: []
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
