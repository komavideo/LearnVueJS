观察属性
=========

## 知识点

* $watch

### $watch

与computed属性类似，用于观察变量的变化，然后进行相应的处理。（我从Angular而来）

~~~html
<div id="myApp">
    <p>今年3月3日发卖的任天堂新一代主机Switch的价格是：{{price}}円，含税价格为：{{priceInTax}}円，折合人民币为：{{priceChinaRMB}}元。</p>
    <button @click="btnClick(10000)">加价10000円</button>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            price: 29980,
            priceInTax: 0,
            priceChinaRMB: 0,
        },
        watch: {
            price: function(newVal, oldVal){
                console.log(newVal, oldVal);
                this.priceInTax = Math.round(this.price * 1.08);
                this.priceChinaRMB = Math.round(this.priceInTax / 16.75);
            },
        },
        methods: {
            btnClick: function(newPrice){
                this.price += newPrice;
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
