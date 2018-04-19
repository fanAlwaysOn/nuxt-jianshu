<template>
    <div id="sign-template">
        <nuxt/>
    </div>
</template>
<script>
    // import Vue from 'vue'
    // import BoostrapVue from 'bootstrap-vue'
    // Vue.use(BoostrapVue)
    // //首先引入bootstrap.css文件，加载bootstrap样式
    // import 'bootstrap/dist/css/bootstrap.css'
    // //引入bootstrap-vue.css文件
    // import 'bootstrap-vue/dist/bootstrap-vue.css'
    export default {

    }
</script>
<style>
    .sign{
        height: 100%;
        font-size: 14px;
        text-align: center;
        background-color: #f1f1f1;
        min-height:750px;
    }
    .sign:before{
        content:'';
        display:inline-block;
        height:85%;
        vertical-align:middle;
    }
    .sign .logo{
        position: absolute;
        left: 50px;
        top: 50px;
    }
    .sign img{
        width: 100px;
    }
    .sign .main{
        border-radius: 4px;
        box-shadow: 0 0 8px rgba(0,0,0,.1);
        width: 400px;
        margin: 60px auto 0;
        padding: 50px 50px 30px;
        background-color: #fff;
        display: inline-block;
        vertical-align: middle;
    }
    .sign .main .title{
        color: #939393;
        margin: 0 auto 30px;
        font-size: 18px;
    }
    .sign .main h4 a{
        font-weight: 400;
        padding: 10px;
        color: #969696;
    }
    .sign .main h4 b{
        font-weight: 800;
        padding: 10px;
        color: #969696;
    }
    .sign .main h4 a.active{
        color: #ea6f5a;
        border-bottom: 2px solid #ea6f5a;
    }
    .sign .main h4 a:hover{
        border-bottom: 2px solid #ea6f5a;
        color: #ea6f5a;
    }
    .sign .main form{
        color: #969696;
        margin: 0 0 30px;
    }
    .sign .main form .input-prepend{
        position: relative;
        width: 100%;
    }
    .sign .main form .input-prepend input{
        width: 100%;
        height: 50px;
        padding: 4px 12px 4px 30px;
        border: 1px solid #c8c8c8;
        border-radius: 2px;
        background-color: rgb(248,248,248);
    }
    .sign .main form .input-prepend:first-of-type input{
        border-bottom: 0;
        border-radius: 4px 4px 0 0;
    }
    .sign .main form .input-prepend:last-of-type input{
        border-bottom:1px solid #c8c8c8;
        border-radius: 0 0 4px 4px;
    }
    .sign .main form .input-prepend i{
        position: absolute;
        font-style: 20px;
        color: #969696;
        left: 15px;
        top: 18px;
    }
    .sign .main form .remeber{
        float: left;
        margin: 20px 0;
    }
    .sign .main form .help{
        float: right;
        margin: 20px 0;
        color: #969696;
    }
    .sign .main form .help:hover{
        color: #333;
    }
    .sign .main form button{
        width: 100%;
        margin: 20px 0 0;
        padding: 9px 18px;
        text-align: center;
        color: #fff;
        border-radius: 30px;
        border: none;
        font-size: 18px;
        outline: none;
        clear: both;
        display:block;
    }
    .sign .main form button.sign-in-btn{
        background-color: #3194d0;
    }
    .sign .main form button.sign-up-btn{
        background-color: #42c02e;
    }
    .sign .main form button.sign-in-btn:hover{
        background-color: rgb(24,124,183);
        cursor:pointer;
    }
    .sign .main form button.sign-up-btn:hover{
        background-color: rgb(61,185,34);
        cursor:pointer;
    }
    .sign .main form p.sign-up-msg{
        font-size:12px;
        margin:15px 0;
        text-align:center;
        line-height:20px;
        color:#969696;
    }
    .sign .main form .ssm{
        position:relative;
        line-height:36px;
    }
    .sign .main form .ssm input{
        border-top:none;
        border-bottom:none;
    }
    .sign .main form .send-ssm{
        position:absolute;
        top:8px;
        right:10px;
        width:100px;
        height:35px;
        line-height:35px;
        border-radius:20px;
        color:#fff;
        text-align:center;
        background:#3db922;
    }
    .sign .main .more-sign p{
        position:relative;
        font-size:14px;
        color:#b8b8b8;
        margin-bottom:20px;
    }
    .sign .main .more-sign p:after{
        content:'';
        width:60px;
        border-bottom:1px solid #b8b8b8;
        position:absolute;
        left:30px;
        top:10px;
    }
    .sign .main .more-sign p:before{
         content:'';
         width:60px;
         border-bottom:1px solid #b8b8b8;
         position:absolute;
         right:10px;
         top:10px;
     }
    .sign .main .more-sign ul{
        display:inline-block;
        color:white;
        margin:0 5px;
        border-radius:50%;
    }
    .sign .main .more-sign ul li{
        display:inline-block;
    }
    .sign .main .more-sign ul li a{
        width:50px;
        height:50px;
        line-height:50px;
        display:block;
    }
    .sign .main .more-sign ul li a i{
        font-size:24px;
        text-alien:center;
        line-height:50px;
    }
    .sign .main .more-sign ul li i.fa-weibo{
        color:#e05244;
    }
    .sign .main .more-sign ul li i.fa-weixin{
        color:#00bb29;
    }
    .sign .main .more-sign ul li i.fa-qq{
        color:#498ad5;
    }
    @media screen and (max-width: 768px){
        .sign .main{
            border:none;
            box-shadow:none;
        }
        html,body{
            background-color:#fff;
        }
        .sign .logo{
            display:none;
        }
        .sign:before{
            height:0;
        }
    }
</style>