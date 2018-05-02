<template>
    <div class="comment-template">
        <my-header title="message"></my-header>
        <div  class="container noticfication">
            <div class="row">
                <!--左边菜单-->
                <div class="col-xs-8 aside">
                    <message-menu title="comment"></message-menu>
                </div>
                <!--右边细节显示-->
                <div class="col-xs-16 col-xs-offset-8 main">
                    <message-detail>
                        <p slot="title" class="title">收到的评论</p>
                        <div slot="info" class="info">
                            <ul>
                                <li @mouseenter="showReport=true">
                                    <nuxt-link to="/">
                                        <img src="~/assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <div class="reply-msg">
                                        <p class="msg">
                                            <nuxt-link to="/">林大傻一号</nuxt-link>在文章
                                            <nuxt-link to="/" class="article">《林大傻传记》</nuxt-link>中写了一条评论
                                        </p>
                                        <p class="time">2018.05.01 18:30</p>
                                    </div>
                                    <p class="reply-info">
                                        <nuxt-link to="/">@隔壁坐个林大傻</nuxt-link> 水水水水水水
                                    </p>
                                    <p class="reply-action">
                                        <nuxt-link to="/"><i class="fa fa-comment-o"></i> 回复</nuxt-link>
                                        <nuxt-link to="/"><i class="fa fa-reply"></i> 查看评价</nuxt-link>
                                        <span class="report" @click="showReportTable=true" v-show="showReport">举报</span>
                                    </p>
                                </li>
                                <li @mouseenter="showReport=true">
                                    <nuxt-link to="/">
                                        <img src="~/assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <div class="reply-msg">
                                        <p class="msg">
                                            <nuxt-link to="/">林大傻一号</nuxt-link>在文章
                                            <nuxt-link to="/" class="article">《林大傻传记》</nuxt-link>中写了一条评论
                                        </p>
                                        <p class="time">2018.05.01 18:30</p>
                                    </div>
                                    <p class="reply-info">
                                        <nuxt-link to="/">@隔壁坐个林大傻</nuxt-link> 水水水水水水
                                    </p>
                                    <p class="reply-action">
                                        <nuxt-link to="/"><i class="fa fa-comment-o"></i> 回复</nuxt-link>
                                        <nuxt-link to="/"><i class="fa fa-reply"></i> 查看评价</nuxt-link>
                                        <span class="report" @click="showReport=true" v-show="showReport">举报</span>
                                    </p>
                                </li>
                                <li @mouseenter="showReport=true">
                                    <nuxt-link to="/">
                                        <img src="~/assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <div class="reply-msg">
                                        <p class="msg">
                                            <nuxt-link to="/">林大傻一号</nuxt-link>在文章
                                            <nuxt-link to="/" class="article">《林大傻传记》</nuxt-link>中写了一条评论
                                        </p>
                                        <p class="time">2018.05.01 18:30</p>
                                    </div>
                                    <p class="reply-info">
                                        <nuxt-link to="/">@隔壁坐个林大傻</nuxt-link> 水水水水水水
                                    </p>
                                    <p class="reply-action">
                                        <nuxt-link to="/"><i class="fa fa-comment-o"></i> 回复</nuxt-link>
                                        <nuxt-link to="/"><i class="fa fa-reply"></i> 查看评价</nuxt-link>
                                        <span class="report" @click="showReport=true" v-show="showReport">举报</span>
                                    </p>
                                </li>
                                <li @mouseenter="showReport=true">
                                    <nuxt-link to="/">
                                        <img src="~/assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <div class="reply-msg">
                                        <p class="msg">
                                            <nuxt-link to="/">林大傻一号</nuxt-link>在文章
                                            <nuxt-link to="/" class="article">《林大傻传记》</nuxt-link>中写了一条评论
                                        </p>
                                        <p class="time">2018.05.01 18:30</p>
                                    </div>
                                    <p class="reply-info">
                                        <nuxt-link to="/">@隔壁坐个林大傻</nuxt-link> 水水水水水水
                                    </p>
                                    <p class="reply-action">
                                        <nuxt-link to="/"><i class="fa fa-comment-o"></i> 回复</nuxt-link>
                                        <nuxt-link to="/"><i class="fa fa-reply"></i> 查看评价</nuxt-link>
                                        <span class="report" @click="showReport=true" v-show="showReport">举报</span>
                                    </p>
                                </li>
                            </ul>
                        </div>
                    </message-detail>
                </div>
            </div>
        </div>
        <!--举报-->
        <div v-show="showReportTable" class="showReport">
            <section>
                <div>
                    <span>举报评论</span>
                    <span class="fa fa-close" @click="showReportTable=false"></span>
                </div>
                <form>
                    <input type="radio" id="ad">
                    <label for="ad">广告及垃圾信息</label>
                    <input type="radio" id="copy">
                    <label for="copy">抄袭或未授权转载</label>
                    <input type="radio" id="others">
                    <label for="others">其它</label>
                    <textarea placeholder="写下举报的详情请看（选填）"></textarea>
                    <input class="submit" type="submit" value="提交" @click.prevent="showReportTable=false">
                    <span @click="showReportTable=false">取消</span>
                </form>
            </section>
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
        },
        data(){
            return{
                showReportTable:false,
                showReport:false,
            }
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
    .noticfication .row .main .info ul{
        margin: 0;
    }
    .noticfication .row .main .info ul li{
        margin: 0;
        padding: 15px;
        border-bottom: 1px solid #f5f5f5;
    }
    .noticfication .row .main .info ul li a img{
        width: 40px;
        height: 40px;
        border-radius: 50%;
        vertical-align: middle;
    }
    .noticfication .row .main .info ul li .reply-msg{
        display: inline-block;
        margin-left: 15px;
        vertical-align: middle;
    }
    .noticfication .row .main .info ul li .reply-msg .msg{
        font-size: 14px;
        color: #000;
    }
    .noticfication .row .main .info ul li .reply-msg .msg .article{
        color: cornflowerblue;
    }
    .noticfication .row .main .info ul li .reply-msg .time{
        font-size: 13px;
        color: gray;
    }
    .noticfication .row .main .info ul li .reply-info{
        margin-top: 10px;
        font-size: 14px;
    }
    .noticfication .row .main .info ul li .reply-info a{
        color: cornflowerblue;
    }
    .noticfication .row .main .info ul li .reply-action{
        color: gray;
        font-size: 13px;
        margin-top: 5px;
    }
    .noticfication .row .main .info ul li .reply-action a{
        color: gray;
        margin-right: 35px;
    }
    .noticfication .row .main .info ul li .reply-action span{
        float: right;
    }
    .noticfication .row .main .info ul li .reply-action span:hover{
        cursor: pointer;
    }
    .showReport{
        width: 100%;
        height: 1000px;
        z-index: 10000;
        /*background: gray;*/
        /*opacity: .9;*/
        background: rgba(255,255,255,.7);
        position: fixed;
        top: 0;
        left: 0;
    }
    .showReport section{
        position: absolute;
        width: 335px;
        margin: 200px 500px;
        padding: 15px;
        background: white;
        /*box-shadow: 2px 2px #7f828b;*/
        border: 2px solid lightgray;
    }
    .showReport section>div{
        display: flex;
        justify-content: space-between;
        flex-wrap: nowrap;
        padding: 5px;
        padding-bottom: 15px;
        border-bottom: 1px solid #f5f5f5;
    }
    .showReport section label{
        font-size: 14px;
    }
    .showReport section form textarea{
        width: 100%;
        height: 60px;
        resize: none;
        margin-top: 10px;
        border-radius: 5px;
        background: #f5f5f5;
    }
    .showReport section form span{
        font-size: 14px;
        color: gray;
        float: right;
        margin-right: 20px;
        margin-top: 14px;
    }
    .showReport section form .submit{
        color: green;
        padding: 4px 9px;
        border: 1px solid green;
        float: right;
        background: #fff;
        border-radius: 15px;
        margin-top: 10px;
    }
    .showReport section form span:hover,.showReport section form .submit:hover{
        cursor: pointer;
    }
</style>