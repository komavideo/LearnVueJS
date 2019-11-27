组件：传递数据
==============

## 知识点

* 为组件传递数据

### 组件数据传递

制作可接受参数的组件。

## 综合例

~~~html
<div id="myApp">
    <h1>您的成绩评价</h1>
    <test-result :score="50"></test-result>
    <test-result :score="65"></test-result>
    <test-result :score="90"></test-result>
    <test-result :score="100"></test-result>
</div>
<script>
    Vue.component('test-result', {
        props: ['score'],
        template: '<div><strong>{{score}}分，{{testResult}}</strong></div>',
        computed: {
            testResult: function() {
                var strResult = "";
                if (this.score < 60)
                    strResult = "不及格";
                else if (this.score < 90)
                    strResult = "中等生";
                else if (this.score <= 100)
                    strResult = "优秀生";
                return strResult;
            }
        }
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
