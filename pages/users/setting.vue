<template>
    <div>
        <my-header></my-header>
        <div class="container setting">
            <div class="row">
                <!--侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside">
                    <ul>
                        <li @click="whichMenu='basic'" :class="whichMenu=='basic'?'active':''">
                            <i class="fa fa-list-ul"></i>
                            基础设置
                        </li>
                        <li  @click="whichMenu='personal'" :class="whichMenu=='personal'?'active':''">
                            <i class="fa fa-user"></i>
                            个人资料
                        </li>
                        <li @click="whichMenu='weibo'" :class="whichMenu=='weibo'?'active':''">
                            <i class="fa fa-weibo"></i>
                            微博验证
                        </li>
                        <li @click="whichMenu='forbidden'" :class="whichMenu=='forbidden'?'active':''">
                            <i class="fa fa-ban"></i>
                            黑名单
                        </li>
                        <li @click="whichMenu='zan'" :class="whichMenu=='zan'?'active':''">
                            <i class="fa fa-dollar"></i>
                            赞赏设置
                        </li>
                        <li @click="whichMenu='login'" :class="whichMenu=='login'?'active':''">
                            <i class="fa fa-cog"></i>
                            账号管理
                        </li>
                    </ul>
                </div>
                <!--主体-->
                <div class="col-xs-16 main">
                    <components :is="whichMenu"></components>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    import basic from '~/components/setting/basic'
    import forbidden from '~/components/setting/forbidden'
    import login from '~/components/setting/login'
    import personal from '~/components/setting/personal'
    import weibo from '~/components/setting/weibo'
    import zan from '~/components/setting/zan'
    export default {
        name: "setting",
        components:{
            myHeader,
            basic,
            forbidden,
            login,
            personal,
            weibo,
            zan
        },
        data(){
            return{
                whichMenu:'basic',
            }
        },
    }
</script>

<style scoped>
    .setting{
        margin-top: 20px;
    }
    .setting .row .aside ul{
        margin: 0;
    }
    .setting .row .aside ul li{
        margin: 0;
        padding: 8px 15px;
        color: #333;
    }
    .setting .row .aside ul li.active{
        background: #f5f5f5;
    }
    .setting .row .aside ul li:hover{
        cursor: pointer;
        background: #f5f5f5;
    }
    .setting .row .aside ul li i{
        width: 32px;
        height: 32px;
        line-height: 32px;
        text-align: center;
        margin-right: 15px;
        background: #a0a0a0;
        border-radius: 5px;
    }
</style>