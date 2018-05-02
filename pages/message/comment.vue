<template>
    <div class="comment-template">
        <my-header></my-header>
        <div  class="container noticfication">
            <div class="row">
                <!--左边菜单-->
                <div class="col-xs-8 aside">
                    <message-menu></message-menu>
                </div>
                <!--右边细节显示-->
                <div class="col-xs-16 col-xs-offset-8 main">
                    <message-detail>
                        <p slot="title" class="title">收到的评论</p>
                        <div slot="info" class="info">
                            <img src="~/assets/img/noInfo.png" alt="没有内容">
                            <p>这里还木有内容哦...</p>
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
        name: "comment",
        components:{
            myHeader,
            messageMenu,
            messageDetail
        }
    }
</script>

<style scoped>
    .comment-template{
        margin-top: 20px;
    }
    .noticfication .row .main{
        margin: 0px;
    }
    .noticfication .row .main .title{
        font-size: 15px;
        padding-bottom:  20px;
        border-bottom: 1px solid #f5f5f5;
    }
    .noticfication .row .main .info{
        margin-top: 150px;
        text-align: center;
    }
    .noticfication .row .main .info img{
        width: 100px;
        vertical-align: middle;
        margin-bottom: 20px;
    }
    .noticfication .row .main .info p{
        font-size: 14px;
        font-weight: 600;
    }
</style>