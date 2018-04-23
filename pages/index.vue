<template>
    <div>
        <my-header></my-header>
        <div class="container index">
            <div class="row">
                <div class="col-xs-16 main">
                    <!--热门专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c1.jpg" alt="">
                            <span class="name">手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c2.jpg" alt="">
                            <span class="name">读书</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c3.jpg" alt="">
                            <span class="name">社会热点</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c4.jpg" alt="">
                            <span class="name">@IT·互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c5.png" alt="">
                            <span name="name">旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c6.jpg" alt="">
                            <span name="name">历史</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c7.jpg" alt="">
                            <span name="name">自然科普</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="more-collection">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                </div>

                <div class="col-xs-offset-1 col-xs-7 aside">
                    侧边栏
                </div>
            </div>
        </div>

    </div>
</template>
<script>
import myHeader from "../components/myHeader.vue"
    export default {
        head:{
            title:"简书-创作你的创作",
            meta:[
                {chartset:"utf-8"},
                {name:"keywords",content:"简书首页"},
                {name:"description",content:"简书首页"},
                {name:"author",content:"范瑞"},
            ]
        },
        components:{
            myHeader
        },
        data () {
            return {
                name:'首页'
            }
        }
    }
</script>
<style>

</style>