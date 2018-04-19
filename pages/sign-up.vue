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
                     <nuxt-link to="/sign-in">登录</nuxt-link>
                     <b>·</b>
                      <nuxt-link class="active" to="/sign-up">注册</nuxt-link>
                 </h4>
            </div>
            <div class="js-form">
                <form action="">
                    <div class="input-prepend">
                        <input type="text" placeholder="你的昵称">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend">
                        <input type="text" placeholder="手机号">
                        <i class="fa fa-mobile fa-lg"></i>
                    </div>
                    <div class="input-prepend ssm">
                        <input type="text" placeholder="手机验证码">
                        <i class="fa fa-shield fa-lg"></i>
                        <a href="#" class="send-ssm">发送验证码</a>
                    </div>
                    <div class="input-prepend">
                        <input type="text" placeholder="设置密码">
                        <i class="fa fa-lock fa-lg"></i>
                    </div>
                    <button class="sign-up-btn">注册</button>
                    <p class="sign-up-msg">
                        点击 “注册” 即表示您同意并愿意遵守简书用户协议 和 隐私政策。
                    </p>
                </form>
            </div>
            <div class="more-sign">
                <p>社交账号直接注册</p>
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
        //设置页面的标题以及描述、关键字等元信息
        name: "sign-up",
        head:{
            //修改当前页面的默认模板为sign.vue,若不写，默认为default.vue
            layout:'sign',
            title:'注册-简书',
            meta:[
                {charset:'utf-8'},
                {name:'keywords',content:'注册页面'},
                {name:'description',content:'注册简书'},
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