<template>
    <div class="chats-template">
        <my-header></my-header>
        <div  class="container noticfication">
            <div class="row">
                <!--左边菜单-->
                <div class="col-xs-8 aside">
                    <message-menu title="other"></message-menu>
                </div>
                <!--右边细节显示-->
                <div class="col-xs-16 col-xs-offset-8 main">
                    <message-detail>
                        <p slot="title" class="title">其它提醒</p>
                        <div slot="info" class="info">

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
        name: "others",
        components:{
            myHeader,
            messageMenu,
            messageDetail
        },
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
</style>