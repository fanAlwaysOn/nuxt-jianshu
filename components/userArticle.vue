<template>
    <div class="userArticle">
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
    </div>
</template>

<script>
    export default {
        name: "userArticle"
    }
</script>

<style>
    .userArticle{
        padding: 15px 0;
    }
    .userArticle ul{
        margin: 0 0 15px 0;

    }
    .userArticle ul li{
        margin: 0;
        padding: 15px 0;
        border-bottom: 1px solid #f5f5f5;
    }
    .userArticle ul li .header{
        display: flex;
        justify-content: left;
        flex-wrap: nowrap;
        margin-bottom: 15px;
    }
    .userArticle ul li .header img{
        width: 32px;
        height: 32px;
        border-radius: 32px;
        margin-right: 20px;
        vertical-align: middle;
    }
    .userArticle ul li .header p{
        vertical-align: middle;
        font-size: 14px;
        line-height: 32px;
    }
    .userArticle ul li .header p span{
        color: gray;
    }
    .userArticle ul li .content{
        margin-top: 15px;
        font-size: 15px;
        margin-bottom: 15px;
    }
    .userArticle ul li .meta a{
        color: #b4b4b4;
        font-size: 13px;
    }
    .userArticle ul li .meta a.origin-author{
        color: #3194d0;
    }
    .userArticle ul li .meta {
        color: #b4b4b4;
        font-size: 13px;
    }
</style>