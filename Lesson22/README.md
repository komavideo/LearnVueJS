表单修饰符
==========

## 知识点

* .lazy
* .number
* .trim

### .lazy

用户输入内容时不做绑定数据的更新处理，在控件的onchange事件中更新绑定的变量。

~~~html
用户名：<input v-model.lazy="username">
~~~

### .number

将用户输入的内容转换为数值类型，如果用户输入非数值的时候，则返回NaN。

~~~html
年龄：<input v-model.number="age" type="number">
~~~

### .trim

自动去掉用户输入内容两端的空格。

~~~html
意见：<input v-model.trim="content">
~~~

## 综合例

~~~html
<div id="myApp">
    <h1>用户注册</h1>
    
    <div>
        <label for="username">用户：</label>
        <input type="text" id="username" v-model.lazy="username" @change="checkUsername">
        <span v-if="checkUsernameOK">可注册</span>
    </div>
    <div>
        <label for="age">年龄：</label>
        <input type="number" id="age" v-model.number="age">
    </div>
    <div>
        <label for="content">个人简介：</label><br/>
        <textarea id="content" v-model.trim="content" cols="55" rows="8"></textarea>
    </div>
    
    <h4>信息区</h4>
    <p>{{username}}</p>
    <p>{{age}}</p>
    <p><pre>{{content}}</pre></p>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp', 
        data: {
            username: "",
            checkUsernameOK: false,
            age: "",
            content: "",
        },
        methods: {
            checkUsername: function(){
                if (this.username.length > 0) this.checkUsernameOK = true;
                else this.checkUsernameOK = false;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
