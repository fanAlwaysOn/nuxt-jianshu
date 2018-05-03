<template>
    <div class="likes">
        <ul>
            <li>
                <nuxt-link to="/">
                    <img src="~/assets/img/collect.jpg" alt="">
                </nuxt-link>
                <div>
                    <p class="user">
                        <img class="head" src="~/assets/img/default-avatar.jpg" alt="">
                        <span class="nickname">晓多</span>
                        <img class="golden" src="~/assets/img/user-golden.jpg" alt="">
                        <span class="date">04.08 21:03</span>
                    </p>
                    <nuxt-link to="/" class="title">“我不是来工作的，是来生活的。”</nuxt-link>
                    <p class="desc">01 晚上10点多从办公室走出来，碰见了也是刚来不久的同事。 外表娇小，个子不高，长相可爱，标准的南方的姑娘，但却还是一个人能抱一大摞资料来回跑出风的姑娘。 我问她这么晚了怎...</p>
                    <p class="meta">
                        <nuxt-link to="/"><i class="fa fa-eye"></i>10&#x3000;</nuxt-link>
                        <nuxt-link to="/"><i class="fa fa-comment"></i>101&#x3000;</nuxt-link>
                        <i class="fa fa-heart"></i>20&#x3000;
                        <i class="fa fa-dollar"></i>10&#x3000;
                        <span>取消收藏</span>
                    </p>
                </div>
            </li>
            <li>
                <nuxt-link to="/">
                    <img src="~/assets/img/collect.jpg" alt="">
                </nuxt-link>
                <div>
                    <p class="user">
                        <img class="head" src="~/assets/img/default-avatar.jpg" alt="">
                        <span class="nickname">晓多</span>
                        <img class="golden" src="~/assets/img/user-golden.jpg" alt="">
                        <span class="date">04.08 21:03</span>
                    </p>
                    <nuxt-link to="/" class="title">“我不是来工作的，是来生活的。”</nuxt-link>
                    <p class="desc">01 晚上10点多从办公室走出来，碰见了也是刚来不久的同事。 外表娇小，个子不高，长相可爱，标准的南方的姑娘，但却还是一个人能抱一大摞资料来回跑出风的姑娘。 我问她这么晚了怎...</p>
                    <p class="meta">
                        <nuxt-link to="/"><i class="fa fa-eye"></i>10&#x3000;</nuxt-link>
                        <nuxt-link to="/"><i class="fa fa-comment"></i>101&#x3000;</nuxt-link>
                        <i class="fa fa-heart"></i>20&#x3000;
                        <i class="fa fa-dollar"></i>10&#x3000;
                        <span>取消收藏</span>
                    </p>
                </div>
            </li>
            <li>
                <nuxt-link to="/">
                    <img src="~/assets/img/collect.jpg" alt="">
                </nuxt-link>
                <div>
                    <p class="user">
                        <img class="head" src="~/assets/img/default-avatar.jpg" alt="">
                        <span class="nickname">晓多</span>
                        <img class="golden" src="~/assets/img/user-golden.jpg" alt="">
                        <span class="date">04.08 21:03</span>
                    </p>
                    <nuxt-link to="/" class="title">“我不是来工作的，是来生活的。”</nuxt-link>
                    <p class="desc">01 晚上10点多从办公室走出来，碰见了也是刚来不久的同事。 外表娇小，个子不高，长相可爱，标准的南方的姑娘，但却还是一个人能抱一大摞资料来回跑出风的姑娘。 我问她这么晚了怎...</p>
                    <p class="meta">
                        <nuxt-link to="/"><i class="fa fa-eye"></i>10&#x3000;</nuxt-link>
                        <nuxt-link to="/"><i class="fa fa-comment"></i>101&#x3000;</nuxt-link>
                        <i class="fa fa-heart"></i>20&#x3000;
                        <i class="fa fa-dollar"></i>10&#x3000;
                        <span>取消收藏</span>
                    </p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "likes"
    }
</script>

<style scoped>
    .likes ul{
        margin: 0;
        width: 100%;
    }
    .likes ul li{
        margin: 0;
        position: relative;
        padding: 15px 0;
        border-bottom: 1px solid #f5f5f5;
    }
    .likes ul li>a{
        display: inline-block;
        position: absolute;
        top: 30px;
        right: 0;
    }
    .likes ul li>a>img{
        width: 150px;
        height: 120px;
    }
    .likes ul li>div{
        display: inline-block;
        width: 76%;
    }
    .likes ul li .user{
        margin: 2px 0 10px;
        font-size: 13px;
    }
    .likes ul li .user img.head{
        width: 32px;
        height: 32px;
        border-radius: 50%;
        vertical-align: middle;
        margin-right: 15px;
    }
    .likes ul li .user img.golden{
        width: 15px;
        vertical-align: middle;
        margin: 0 8px;
    }
    .likes ul li .user .date{
        color: gray;
    }
    .likes ul li .title{
        margin: 10px 0;
        display: block;
    }
    .likes ul li .desc{
        font-size: 14px;
        margin-bottom: 10px;
    }
    .likes ul li .meta a{
        color: #b4b4b4;
        font-size: 13px;
    }
    .likes ul li .meta a.origin-author{
        color: #3194d0;
    }
    .likes ul li .meta {
        color: #b4b4b4;
        font-size: 13px;
    }
</style>