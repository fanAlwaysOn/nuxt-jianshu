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
        </ul>
    </div>
</template>

<script>
    export default {
        name: "userHot"
    }
</script>

<style scoped>

</style>