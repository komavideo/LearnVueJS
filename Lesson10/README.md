设定计算属性
============

## 知识点

* setter

### setter

设置计算属性，同步更新元数据的值。（又是令人费解的描述）

~~~html
<div id="myApp">
    <p>今年3月3日发卖的任天堂新一代主机Switch的价格是：{{price}}円，含税价格为：{{priceInTax}}円，折合人民币为：{{priceChinaRMB}}元。</p>
    <button @click="btnClick(10800)">把含税改价为10800円</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            price: 29980
        },
        computed: {
            priceInTax: {
                get:function(){
                    return this.price * 1.08;
                },
                set: function(value){
                    this.price = value / 1.08;
                }
            },
            priceChinaRMB: function(){
                return Math.round(this.priceInTax / 16.75);
            },
        },
        methods: {
            btnClick: function(newPrice){
                this.priceInTax = newPrice;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
