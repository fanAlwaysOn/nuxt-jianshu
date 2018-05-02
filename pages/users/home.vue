<template>
    <div>
        <my-header></my-header>
        <div class="container index">
            <div class="row">
                <!--主体内容-->
                <div class="col-xs-16 main" style="background: #eeeeee;height: 500px;">
                    <!--个人内容-->
                    <div>
                        <a href='javascript(0)' class="img">
                            <img src="~/assets/img/default-avatar.jpg" alt="">
                        </a>
                        <div class="detail-info">
                            <p class="nickname">吹吹</p>
                            <ul>
                                <li>
                                    <nuxt-link to="/">
                                        <p>12</p>
                                        <p>关注 <i class="fa fa-angle-right"></i></p>
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/">
                                        <p>12</p>
                                        <p>粉丝 <i class="fa fa-angle-right"></i></p>
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/">
                                        <p>11342</p>
                                        <p>文章 <i class="fa fa-angle-right"></i></p>
                                    </nuxt-link>
                                </li>
                                <li>
                                    <p>1222</p>
                                    <p>字数 <i class="fa fa-angle-right"></i></p>
                                </li>
                                <li>
                                    <p>1322</p>
                                    <p>收获喜欢 <i class="fa fa-angle-right"></i></p>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <ul>
                        <li @click="selectMenu='userArticle'" :class="selectMenu=='userArticle'?'active':''">
                            <i class="fa fa-"></i>
                            文章
                        </li>
                        <li @click="selectMenu='userDynanic'" :class="selectMenu=='userDynanic'?'active':''">
                            <i class="fa fa-"></i>
                            动态
                        </li>
                        <li @click="selectMenu='userComment'" :class="selectMenu=='userComment'?'active':''">
                            <i class="fa fa-"></i>
                            最新评论
                        </li>
                        <li @click="selectMenu='userHot'" :class="selectMenu=='userHot'?'active':''">
                            <i class="fa fa-"></i>
                            热门
                        </li>
                    </ul>
                    <!--<transition enter-active-class="animated fadeInRight" leave-active-class="animated fadeOutLeft" mode="out-in">-->
                    <transition name="fade">
                        <component :is="selectMenu"></component>
                    </transition>
                </div>
                <!--侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside">
                    <ul>
                        <li>
                            <i class="fa fa-menu"></i>
                            我关注的专题/文集/连载
                        </li>
                        <li>
                            <i class="fa fa-heart-o"></i>
                            我喜欢的文章
                        </li>
                        <li>我创建的专题</li>
                        <li>
                            <i class="fa fa-plus"></i>
                            创建一个新专题
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
    import myHeader from '~/components/myHeader'
    import userArticle from '~/components/userArticle'
    import userDynanic from '~/components/userDynanic'
    import userComment from '~/components/userComment'
    import userHot from '~/components/userHot'

    export default {
        name: "home",
        components: {
            myHeader,
            userArticle,
            userDynanic,
            userComment,
            userHot
        },
        data() {
            return {
                selectMenu: 'userArticle',
            }
        }
    }
</script>

<style scoped>
    .index .row .main{
        background: #fff!important;
    }
    .index .row .main>ul{
        margin: 0;
    }
    .index .row .main>ul>li{
        display: inline-block;
        /*margin-left: 30px;*/
        padding: 17px 30px;
    }
    .index .row .main>ul>li.active{
        border-bottom: 2px solid black;
    }
    .index .row .main>ul>li:hover{
        cursor: pointer;
    }
    .index .row .main .img{
        width: 80px;
        height: 80px;
    }
    .index .row .main .img img{
        /*width: 100%;*/
        /*height: 100%;*/
        border-radius: 50%;
        vertical-align: middle;
        display: inline-block;
        margin-right: 20px;
    }
    .index .row .main .detail-info{
        display: inline-block;
        vertical-align: middle;
    }
    .index .row .main .detail-info .nickname{
        font-size: 21px;
        font-weight: 700;
    }
    .index .row .main .detail-info ul{
        margin: 0px;
    }
    .index .row .main .detail-info ul li{
        margin: 0px;
        padding-right: 10px;
        border-right: 1px solid #f5f5f5;
        margin-right: 10px;
        display: inline-block;
    }
    .index .row .main .detail-info ul li a:hover{
        cursor: pointer;
    }
    .index .row .main .detail-info ul li p:nth-of-type(2){
        font-size: 12px;
    }
    .index .row .aside {
        margin-top: 20px;
    }
    .index .row .aside ul{
        margin: 0;
    }
    .index .row .aside li{
        margin: 0;
        padding: 15px 10px;
        font-size: 14px;
    }
    .index .row .aside li:nth-of-type(1){
        border-top: 1px solid #f5f5f5;
        padding-top: 15px;
    }
    .index .row .aside li:nth-of-type(2){
        border-bottom: 1px solid #f5f5f5;
    }
    .index .row .aside li:nth-of-type(3){
        color: gray;
    }
    .index .row .aside li:nth-of-type(4){
        color: green;
        padding-top: 0;
    }
    .fade-enter-active, .fade-leave-active {
        transition: all .8s;
    }
    .fade-enter-to, .fade-leave {
        width: 100%;
    }
    .fade-enter, .fade-leave-to {
        width: 0px;
    }

    /*.fade-enter-active {*/
    /*animation: inn 2s;*/
    /*}*/

    /*.fade-leave-active {*/
    /*animation: out .5s;*/
    /*}*/

    /*@keyframes inn {*/
    /*0% {*/
    /*transform: translate(100%);*/
    /*}*/
    /*50%{*/
    /*transform:translate(50%);*/
    /*}*/
    /*100% {*/
    /*transform: translate(0%);*/
    /*}*/
    /*}*/

    /*@keyframes out {*/
    /*0% {*/
    /*transform: translateX(0%);*/
    /*}*/
    /*100% {*/
    /*transform: translateX(-100%);*/
    /*}*/
    /*}*/
</style>