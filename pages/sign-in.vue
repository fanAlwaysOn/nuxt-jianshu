<template>
    <div class="sign">
        <div class="logo">
            <nuxt-link to="/">
                <img src="~assets/img/logo.png">
            </nuxt-link>
        </div>
        <div class="main">
            <div class="title">
                <h4>
                    <nuxt-link class="active" to="/sign-in">登录</nuxt-link>
                    <b>·</b>
                    <nuxt-link class="activea" to="/sign-up">注册</nuxt-link>
                </h4>
            </div>
            <div class="js-form">
                <form action="">
                    <div class="input-prepend">
                        <input type="text" placeholder="手机号或邮箱">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend">
                        <input type="text" placeholder="密码">
                        <i class="fa fa-lock"></i>
                    </div>
                    <div class="remeber">
                        <input type="checkbox">
                        <span>记住我</span>
                    </div>
                    <div class="help">
                        <nuxt-link to="/">登录遇到问题</nuxt-link>
                    </div>

                    <button class="sign-in-btn">登录</button>
                </form>
            </div>
            <div class="more-sign">
                <p>社交账号登录</p>
                <ul>
                    <li>
                        <nuxt-link to="/">
                            <i class="fa fa-weixin"></i>
                        </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/">
                            <i class="fa fa-weibo"></i>
                        </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/">
                            <i class="fa fa-qq"></i>
                        </nuxt-link>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        //修改当前页面的默认模板为sign.vue,若不写，默认为default.vue
        layout:'sign',
        //设置页面的标题以及描述、关键字等元信息
        name: "sign-in",
        head:{
            title:'登录-简书',
            meta:[
                {charset:'utf-8'},
                {name:'keywords',content:'登录页面'},
                {name:'description',content:'登录简书'},
                {name:'author',content:'范瑞'}
            ]
        },
        data () {
            return {

            }
        }
    }
</script>

<style scoped>

</style>