计算属性
=========

## 知识点

* computed

### computed

处理元数据，便于进行二次利用。（比如：消费税自动计算功能）

~~~html
<div id="myApp">
    今年3月3日发卖的任天堂新一代主机Switch的价格是：{{price}}円，含税价格为：{{priceInTax}}円，折合人民币为：{{priceChinaRMB}}元。
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            price: 29980
        },
        computed: {
            priceInTax: function(){
                return this.price * 1.08;
            },
            priceChinaRMB: function(){
                return Math.round(this.priceInTax / 16.75);
            },
        },
    });
</script>
~~~

## 源文件

* https://gitee.com/komavideo/LearnVueJS

## 小马视频频道

http://komavideo.com
