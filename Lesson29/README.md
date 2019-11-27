组件：参数验证
==============

## 知识点

* props:组件参数验证语法

### 组件的数据

为组件中接受到的变量进行逻辑验证。

## 综合例

~~~html
<div id="myApp">
    <h1>身世之谜</h1>
    <show-member-info name="koma" :age="25" :detail="{address:'earth', language:'世界语'}"></show-member-info>
</div>
<script>
    Vue.component('show-member-info', {
        props: {
            name: {
                type: String,
                required: true,
            },
            age: {
                type: Number,
                validator: function (value) {
                    return value >= 0 && value <= 130;
                }                
            },
            detail: {
                type: Object,
                default: function() {
                    return {
                        address: 'US',
                        language: 'English',
                    };
                }
            },
        },
        template: '<div>姓名：{{this.name}}<br/>' 
            + '年龄：{{this.age}}岁<br/>'
            + '地址：{{this.detail.address}}<br/>'
            + '语言：{{this.detail.language}} </div>',
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
