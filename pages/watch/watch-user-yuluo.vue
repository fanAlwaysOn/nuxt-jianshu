<template>
    <div>
        <my-header></my-header>
        <div class="container watch">
            <div class="row">
                <!--左边侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside">
                    <watch-menu></watch-menu>
                </div>
                <!--右方内容-->
                <div class="col-xs-16 main">
                    <!--头部-->
                    <header>
                        <nuxt-link to="/" class="header">
                            <img src="~/assets/img/default-avatar.jpg" alt="">
                        </nuxt-link>
                        <nuxt-link to="/" class="index">
                            个人主页&nbsp;
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                        <nuxt-link to="/" class="send-msg">
                            发简信
                        </nuxt-link>
                        <div class="title">
                            <nuxt-link to="/">雨落黄岩</nuxt-link>
                            <img src="~/assets/img/watch-right-good.jpg" alt="">
                            <i class="fa fa-venus"></i>
                            <div class="info">写了236992字，获得了2127个喜欢</div>
                        </div>
                    </header>
                    <!--导航-->
                    <ul class="menu">
                        <li @click="whichMenu='newPublish'" :class="whichMenu=='newPublish'?'active':''">
                            <i class="fa fa-file-text"></i>
                            最新发布
                        </li>
                        <li @click="whichMenu='newComment'" :class="whichMenu=='newComment'?'active':''">
                            <i class="fa fa-comments"></i>
                            最新评论
                        </li>
                        <li @click="whichMenu='hotPublish'" :class="whichMenu=='hotPublish'?'active':''">
                            <i class="fa fa-fire"></i>
                            热门最新发布
                        </li>
                    </ul>
                    <transition>
                        <component :is="whichMenu"></component>
                    </transition>
                    <a href="javascript(0)" class="load-more">阅读更多</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    import watchMenu from '~/components/watchMenu'
    import newPublish from '~/components/watchRightMenu/newPublish'
    import newComment from '~/components/watchRightMenu/newComment'
    import hotPublish from '~/components/watchRightMenu/hotPublish'
    export default {
        name: "watch-user-yuluo",
        components: {
            myHeader,
            watchMenu,
            newPublish,
            newComment,
            hotPublish
        },
        data(){
            return{
                whichMenu:'newPublish',
            }
        }
    }
</script>

<style scoped>
    @import "../../assets/css/watchRightMain.css";
</style>