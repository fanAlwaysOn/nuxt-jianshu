<template>
    <div class="chats-template">
        <my-header></my-header>
        <div  class="container noticfication">
            <div class="row">
                <!--左边菜单-->
                <div class="col-xs-8 aside">
                    <message-menu title="chats"></message-menu>
                </div>
                <!--右边细节显示-->
                <div class="col-xs-16 col-xs-offset-8 main">
                    <message-detail>
                        <p slot="title" class="title">全部简信</p>
                        <div slot="info" class="info">
                            <ul>
                                <li>
                                    <div class="time">
                                        <span>
                                            05.02 18:20
                                            <i class="fa fa-angle-down" @click="showMenu=!showMenu"></i>
                                        </span>
                                        <div v-show="showMenu" class="hidden-menu">
                                            <ul>
                                                <li>
                                                    <i class="fa fa-university"></i>
                                                    删除会话
                                                </li>
                                                <li>
                                                    <i class="fa fa-window-close"></i>
                                                    加入黑名单
                                                </li>
                                                <li>
                                                    <i class="fa fa-repeat"></i>
                                                    不知道是啥
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <nuxt-link to="/" class="img">
                                        <img src="~/assets/img/message-chat.png" alt="">
                                        <span>1</span>
                                    </nuxt-link>
                                    <div class="desc">
                                        <nuxt-link to="/">
                                            <p>
                                                简宝玉
                                            </p>
                                            <p>欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点...</p>
                                        </nuxt-link>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </message-detail>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    import messageMenu from '~/components/messageMenu'
    import messageDetail from '~/components/messageDetail'
    export default {
        name: "chats",
        components:{
            myHeader,
            messageMenu,
            messageDetail
        },
        data(){
            return{
                showMenu:false,
            }
        }
    }
</script>

<style scoped>
    .chats-template{
        margin-top: 20px;
    }
    .noticfication .row .main{
        margin: 0px;
    }
    .noticfication .row .main .title{
        font-size: 15px;
        padding: 10px;
        padding-bottom:  20px;
        border-bottom: 1px solid #f5f5f5;

    }
    .noticfication .row .main .info ul li{
        position: relative;
    }
    .noticfication .row .main .info ul li .time{
        float: right;
        font-size: 14px;
        color: gray;
        position: relative;
    }
    .noticfication .row .main .info ul li .time span i:hover{
        cursor: pointer;
    }
    .noticfication .row .main .info ul li .time .hidden-menu{
        padding: 8px 0;
        position: absolute;
        background: #fff;
        top: 25px;
        border: 1px solid #f2f2f2;
    }
    .noticfication .row .main .info ul li .time .hidden-menu ul{
        margin: 0px;
        width: 140px;
    }
    .noticfication .row .main .info ul li .time .hidden-menu ul li{
        margin: 0;
        padding: 8px 13px;
    }
    .noticfication .row .main .info ul li .time .hidden-menu ul li:hover{
        cursor: pointer;
    }
    .noticfication .row .main .info ul li .time .hidden-menu ul li:hover{
        background: #f5f5f5;
    }
    .noticfication .row .main .info ul li .time .hidden-menu ul li i{
        margin-right: 10px;
    }
    .noticfication .row .main .info ul li .img{
        position: relative;
    }
    .noticfication .row .main .info ul li .img img{
        width: 48px;
        height: 48px;
        border-radius: 50%;
        vertical-align: middle;
    }
    .noticfication .row .main .info ul li .img span{
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: #ea6f5a;
        color: #fff;
        text-align: center;
        position: absolute;
        right: 1px;
    }
    .noticfication .row .main .info ul li .desc{
        margin-left: 58px;
        display: inline-block;
        position: absolute;
        left: 10px;
        top: 7px;
    }
    .noticfication .row .main .info ul li .desc a p{
        font-size: 14px;
        color: gray;
    }
    .noticfication .row .main .info ul li .desc a p:nth-of-type(1){
        color: #000;
        font-size: 15px;
    }
</style>