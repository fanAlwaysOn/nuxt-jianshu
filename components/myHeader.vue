<template>
    <div style="height:100%">
        <nav class="navbar navbar-fixed-top">
            <div class="width-limit">
                <nuxt-link class="logo" to="/">
                    <img src="~/assets/img/nav-logo.png">
                </nuxt-link>
                <nuxt-link to="/write" class="write-btn">
                    <i class="fa fa-edit"></i>
                    写文章
                </nuxt-link>
                <div class="user" @mouseleave="isShow=false">
                    <div class="drop-down" @mouseenter="isShow=true">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="~/assets/img/default-avatar.jpg">
                        </nuxt-link>
                    </div>
                    <ul class="drop-menu" v-show="isShow">
                        <li>
                            <nuxt-link to="">
                                <i class="fa fa-home"></i>
                                我的主页
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/user/123/like">
                                <i class="fa fa-heart"></i>
                                喜欢的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/bookmarks">
                                <i class="fa fa-bookmark"></i>
                                收藏的文章
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
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
            </div>
        </nav>
    </div>
</template>
<script>
    export default {
        name: "myHeadder",
        data: function () {
            return {
                isShow: false,
            }
        },
    }
</script>
<style scoped>
    nav {
        height: 56px;
        width: 100%;
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

    nav .user .drop-down {

    }

    nav .user .drop-menu {
        position: absolute;
        left: 0;
        box-shadow: 0 0 8px rgba(0, 0, 0, .1);
        min-width: 160px;
        z-index: 999;
        margin: 0;
        padding: 10px 0px;
        font-size: 15px;
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
</style>