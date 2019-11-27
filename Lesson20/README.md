表单单选按钮
============

## 知识点

* v-model
* input[type="radio"]

### 表单单选按钮绑定

~~~html
<div id="myApp">
    <h1>表单单选按钮</h1>

    <h3>选择性别</h3>
    <input type="radio" id="male" value="男" v-model="pickedSex">
    <label for="male">男</label>
    <br>
    <input type="radio" id="female" value="女" v-model="pickedSex">
    <label for="female">女</label>

    <h3>选择爱好</h3>
    <input type="radio" id="game" value="玩游戏" v-model="pickedHobby">
    <label for="game">玩游戏</label>
    <br>
    <input type="radio" id="movie" value="看电影" v-model="pickedHobby">
    <label for="movie">看电影</label>

    <h3>选择结果</h3>
    <p>性别: {{ pickedSex }}</p>
    <p>爱好: {{ pickedHobby }}</p>

</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            pickedSex: "",
            pickedHobby: "",
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
