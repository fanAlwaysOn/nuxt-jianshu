<template>
    <div style="height:100%">
        <nav class="navbar navbar-fixed-top">
            <div class="width-limit">
                <!--logo-->
                <nuxt-link class="logo" to="/">
                    <img src="~/assets/img/nav-logo.png">
                </nuxt-link>
                <!--右上角，写文章-->
                <nuxt-link to="/write" class="write-btn">
                    <i class="fa fa-edit"></i>
                    写文章
                </nuxt-link>
                <!--登录用户信息-->
                <div class="user" @mouseleave="UserShow=false">
                    <div class="drop-down" @mouseenter="UserShow=true">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="~/assets/img/default-avatar.jpg">
                        </nuxt-link>
                    </div>
                    <ul class="drop-menu" v-show="UserShow">
                        <li>
                            <nuxt-link to="/users/home">
                                <i class="fa fa-home"></i>
                                我的主页
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/users/like">
                                <i class="fa fa-heart"></i>
                                喜欢的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/users/collected">
                                <i class="fa fa-bookmark"></i>
                                收藏的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/users/setting">
                                <i class="fa fa-cog"></i>
                                设置
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
                                <i class="fa fa-sign-out"></i>
                                退出
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <!--右上角，登录注册-->
                <!--导航部分-->
                <div class="container">
                    <div class="row">
                        <!--隐藏菜单按钮-->
                        <div class="menu" @click="showMenuList()">
                            <i class="fa fa-align-justify"></i>
                        </div>
                        <!--隐藏的菜单选项-->
                        <!--<transition name="fade">-->
                        <transition enter-active-class="animated fadeInDown" leave-active-class="animated fadeOutUp">
                            <ul class="hidden-menu-list" v-show="menuListShow">
                                <li>发现</li>
                                <li>关注</li>
                                <li>消息</li>
                                <li>
                                    <form action="">
                                        <input type="text" placeholder="搜索" class="menu-search">
                                        <a href="#" class="search-btn">
                                            <i class="fa fa-search"></i>
                                        </a>
                                    </form>
                                </li>
                            </ul>
                        </transition>
                        <ul class="nav-list">
                            <li @click="navList='find'">
                                <nuxt-link to="/" :class="navList=='find'?'active':''">
                                    <i class="fa fa-compass"></i>
                                    <span>发现</span>
                                </nuxt-link>
                            </li>
                            <li @click="navList='watch'">
                                <nuxt-link to="/watch/watch" :class="navList=='watch'?'active':''">
                                    <i class="fa fa-book"></i>
                                    <span>关注</span>
                                </nuxt-link>
                            </li>
                            <li class="user" @mouseover="notifyShow=true" @mouseout="notifyShow=false"
                                @click="navList='message'">
                                <nuxt-link to="/message/comment" :class="navList=='message'?'active':''">
                                    <i class="fa fa-bell-o"></i>
                                    <span>消息</span>
                                </nuxt-link>
                                <ul class="drop-menu" v-show="notifyShow">
                                    <li>
                                        <nuxt-link to="/message/comment">
                                            <i class="fa fa-comment-o"></i>
                                            评论
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="">
                                            <i class="fa fa-envelope-o"></i>
                                            简讯
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="">
                                            <i class="fa fa-plus-square-o"></i>
                                            关注
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="">
                                            <i class="fa fa-heart-o"></i>
                                            喜欢和赞
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="">
                                            <i class="fa fa-ellipsis-h"></i>
                                            其它提醒
                                        </nuxt-link>
                                    </li>
                                </ul>
                            </li>
                            <li class="search">
                                <form method="post">
                                    <input type="text" placeholder="搜索" class="search-input">
                                    <a href="#" class="search-btn">
                                        <i class="fa fa-search"></i>
                                    </a>
                                </form>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
    export default {
        name: "myHeadder",
        props:["title"],
        data: function () {
            return {
                UserShow: false,
                notifyShow: false,
                menuListShow: false,
                navList:'',
            }
        },
        methods: {
            showMenuList: function () {
                this.menuListShow = !this.menuListShow;
            }
        },
        mounted:function () {
            this.navList=this.title;
        }
    }
</script>
<style scoped>
    .fade-enter-active, .fade-leave-active {
        transition: all .5s;
    }
    .fade-enter, .fade-leave-to {
        height: 0px;
    }
    .fade-enter-to, .fade-leave {
        height: 206px;
    }
    nav {
        height: 56px;
        width: 100%;
        background: white;
    }
    .navbar {
        margin-bottom: 20px;
        border-width: 0 0 1px;
        border-color: #f0f0f0;
        border-bottom: 1px solid #f0f0f0;
    }
    .navbar:before {
        content: "";
        display: table;
    }
    .navbar-fixed-top {
        position: fixed;
        left: 0;
        top: 0;
        z-index: 9999;
    }
    nav .width-limit {
        min-width: 768px;
        max-width: 1200px;
        height: 56px;
        margin: 0 auto;
    }
    nav .log {
        display: block;
    }
    nav .logo img {
        max-width: 100%;
        height: 100%;
        float: left;
        display: block;
    }
    nav .write-btn {
        float: right;
        width: 100px;
        height: 40px;
        line-height: 40px;
        margin: 8px 15px 0;
        border-radius: 15px;
        color: #fff;
        background: #ea6f5a;
        text-align: center;
    }
    nav .write-btn:hover {
        background-color: #ec6149;
    }
    nav .user {
        position: relative;
        float: right;
    }
    nav .user .avatar {
        width: 40px;
        height: 40px;
        margin: 8px 28px 8px 20px;
        display: block;
        position: relative;
    }
    nav .user .drop-down:hover {
        background: #f5f5f5;
    }
    nav .user .avatar:before {
        content: "";
        position: absolute;
        top: 18px;
        right: -16px;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 5px solid #999;
    }
    nav .user .avatar img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        border: 1px solid #eee;
    }
    nav .user .drop-menu {
        position: absolute;
        left: 0;
        box-shadow: 0 0 8px rgba(0, 0, 0, .1);
        min-width: 160px;
        margin: 0;
        padding: 10px 0px;
        font-size: 15px;
        z-index: 9999;
        background: white;
    }
    nav .user .drop-menu li a {
        padding: 10px 20px;
        display: block;
        line-height: 30px;
    }
    nav .user .drop-menu li a:hover {
        background: #f5f5f5;
    }
    nav .user .drop-menu li a i {
        margin-right: 15px;
        color: #ea6f5a;
        width: 20px;
        height: 20px;
        font-size: 20px;
        display: inline-block;
    }
    /********隐藏********/
    nav .menu {
        display: none;
    }
    nav .menu > i {
        padding: 5px;
    }
    nav .menu > i:hover {
        padding: 5px;
        border: 1px solid #eee;
        background: #eee;
    }
    nav .hidden-menu-list {
        width: 100%;
        margin: 0;
        z-index: -999;
        background-color: white;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        position: fixed;
        left: 0;
        top: 56px;
    }
    nav .hidden-menu-list li {
        width: 100%;
        font-size: 20px;
        color: gray;
        text-align: center;
        padding: 10px;
        border-bottom: 1px solid #eee;
    }
    nav .hidden-menu-list li:nth-of-type(-n+3):hover {
        background: #eee;
        cursor: pointer;
    }
    nav .hidden-menu-list li input {
        height: 38px;
        width: 100%;
        font-size: 14px;
        padding: 0 40px 0 20px;
        border: 1px solid #eee;
        background: #eee;
        border-radius: 40px;
        position: relative;
    }
    nav .hidden-menu-list .search-btn {
        position: absolute;
        width: 30px;
        height: 30px;
        bottom: 14px;
        right: 19px;
        color: #969696;
        text-align: center;
        padding: 0;
    }
    nav .hidden-menu-list .menu-search:focus + .search-btn {
        background: rgb(150, 150, 150);
        color: #fff;
        border-radius: 50%;
    }
    nav .hidden-menu-list .menu-search i {
        display: block !important;
        margin: 0;
        text-align: center;
        line-height: 30px;
        font-size: 14px;

    }
    nav .nav-list {
        margin: 0;
    }
    nav .nav-list:after {
        content: '';
        height: 0;
        display: block;
        visibility: hidden;
        clear: both;
    }
    nav .nav-list > li {
        float: left;
        margin-right: 5px;
    }
    nav .nav-list > li a {
        display: block;
        height: 56px;
        /*line-height: 26px;*/
        padding: 15px;
    }
    nav .nav-list > li a.active {
        color: #ea6f5a;
        background: none !important;
    }
    nav .nav-list > li a:hover {
        background: #f5f5f5;
    }
    nav .nav-list > li a i {
        margin-right: 5px;
        font-size: 20px;
    }
    nav .nav-list .search {
        padding-left: 15px;
        margin-left: 10px;
    }
    nav .nav-list .search form {
        position: relative;
        margin-bottom: 20px;
        top: 9px;
    }
    nav .nav-list .search form .search-input {
        width: 240px;
        height: 38px;
        font-size: 14px;
        padding: 0 40px 0 20px;
        border: 1px solid #eee;
        background: #eee;
        border-radius: 40px;
        transition: width .5s;
    }
    nav .nav-list .search form .search-input:focus {
        width: 320px;
    }
    nav .nav-list .search form .search-input:focus + .search-btn {
        background: #969696;
        color: #fff;
        border-radius: 50%;
    }
    nav .nav-list .search form .search-input:blur {
        width: 240px;
    }
    nav .nav-list .search form .search-btn {
        position: absolute;
        width: 30px;
        height: 30px;
        top: 4px;
        right: 7px;
        color: #969696;
        text-align: center;
        padding: 0;
    }
    nav .nav-list .search form .search-btn:hover {
        background: none;
    }
    nav .nav-list .search form .search-btn i {
        display: block !important;
        margin: 0;
        text-align: center;
        line-height: 30px;
        font-size: 14px;
    }

    @media (max-width: 1200px) {
        nav .nav-list > li a > i {
            display: none;
        }

        nav .nav-list .search-input {
            width: 160px;
        }

        nav .nav-list .search form .search-input:focus {
            width: 240px;
        }
    }

    @media (max-width: 900px) {
        nav .nav-list li span {
            display: none;
        }

        nav .nav-list li a i {
            display: block;
        }
    }

    @media (max-width: 768px) {
        nav .nav-list {
            display: none;
        }

        nav .menu {
            display: block;
            color: gray;
            line-height: 56px;
            font-size: 20px;
        }

        /*nav .hidden-menu-list{*/
        /*display: block;*/
        /*}*/
    }

    @media (min-width: 768px) {
        nav .hidden-menu-list {
            display: none;
        }
    }
</style>