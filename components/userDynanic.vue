<template>
    <div class="userArticle userDynanic">
        <ul>
            <li>
                <div class="header">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                    <p>吹吹 <span>几秒前</span></p>
                </div>
                <nuxt-link to="/" class="date">2018-05-03</nuxt-link>
                <p class="content">哈哈哈哈哈哈哈哈哈哈哈哈</p>
                <p class="meta">
                    <nuxt-link to="/"><i class="fa fa-eye"></i>10&#x3000;</nuxt-link>
                    <nuxt-link to="/"><i class="fa fa-comment"></i>101&#x3000;</nuxt-link>
                    <i class="fa fa-heart"></i>20&#x3000;
                </p>
            </li>
        </ul>
        <ul class="section">
            <li>
                <div class="header">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                    <p>吹吹 <span>关注了作者 · 04.20 09:02</span></p>
                </div>
                <section>
                    <p class="followed">已关注</p>
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                    <div>
                        <p>阿里云云栖社区</p>
                        <p>写了 2761881 字，被 239134 人关注，获得了 17794 个喜欢</p>
                    </div>
                    <p class="abstruct">汇集阿里技术精粹，http://yq.aliyun.com 欢迎关注：官方微博@阿里云云栖社区 官方微信号 yunqiinsight</p>
                </section>
            </li>
            <li>
                <div class="header">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                    <p>吹吹 <span>关注了作者 · 04.20 09:02</span></p>
                </div>
                <section>
                    <p class="followed">已关注</p>
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                    <div>
                        <p>腾讯</p>
                        <p>写了 2761881 字，被 239134 人关注，获得了 17794 个喜欢</p>
                    </div>
                    <p class="abstruct">欢迎关注：官方微博@阿里云云栖社区 官方微信号 yunqiinsight</p>
                </section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "userDynanic"
    }
</script>

<style scoped>
    .userDynanic .section{
        padding: 15px 0;
    }
    .userDynanic .section li section{
        border: 1px solid lightgray;
        padding: 15px;
    }
    .userDynanic .section li section .followed{
        float: right;
        vertical-align: middle;
    }
    .userDynanic .section li section img{
        width: 48px;
        height: 48px;
        border-radius: 50%;
        vertical-align: middle;
    }
    .userDynanic .section li section div{
        margin-left: 20px;
        display: inline-block;
        vertical-align: middle;
    }
    .userDynanic .section li section div>p:nth-of-type(2){
        font-size: 13px;
        color: gray;
        margin-top: 4px;
    }
    .userDynanic .section li section .abstruct{
        margin: 20px 0;
        font-size: 13px;
        padding-top: 20px;
        border-top: 1px solid #f5f5f5;
        color: gray;
    }
</style>