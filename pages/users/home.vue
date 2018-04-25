<template>
    <div>
        <my-header></my-header>
        <div class="container index">
            <div class="row">
                <!--主体内容-->
                <div class="col-xs-16 main" style="background: #eeeeee;height: 500px;">
                    <div>头部</div>
                    <ul>
                        <li @click="selectMenu='userArticle'">文章</li>
                        <li @click="selectMenu='userDynanic'">动态</li>
                        <li @click="selectMenu='userComment'">最新评论</li>
                        <li @click="selectMenu='userHot'">热门</li>
                    </ul>
                    <!--<transition enter-active-class="animated fadeInRight" leave-active-class="animated fadeOutLeft" mode="out-in">-->
                    <transition name="fade">
                        <component :is="selectMenu"></component>
                    </transition>
                </div>
                <!--侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside" style="background: pink;height: 500px;"></div>
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
                selectMenu: userArticle,
            }
        }
    }
</script>

<style scoped>
    ul > li {
        display: inline-block;
        margin-left: 20px;
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