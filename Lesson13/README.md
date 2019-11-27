条件渲染
=========

## 知识点

* v-if
* v-else-if
* v-else

### v-if

判断vue.js的变量的值，然后执行页面渲染逻辑。（if-elseif-else）

~~~html
<div id="myApp">
    <h1 v-if="result == 0">成绩未公布</h1>
    <h1 v-else-if="result < 60">{{result}}分 - 考试不及格</h1>
    <h1 v-else-if="result < 80">{{result}}分 - 还需努力</h1>
    <h1 v-else>{{result}}分 - 考得不错，玩游戏吧！</h1>
    <button @click="btnClick">考试成绩</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            result: 0
        },
        methods: {
            btnClick: function(){
                this.result = Math.round(Math.random() * 100);
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
