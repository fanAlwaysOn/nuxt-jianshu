<template>
    <div class="followed">
        <ul>
            <li>
                <p>
                    <i class="fa fa-checked"></i>
                    已关注
                </p>
                <nuxt-link to="/" class="img">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="desc">
                    <p class="title">社会热点</p>
                    <p><span>简书</span> 收录了47489篇文章，1356636人关注</p>
                </div>
            </li>
            <li>
                <p>
                    <i class="fa fa-checked"></i>
                    已关注
                </p>
                <nuxt-link to="/" class="img">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="desc">
                    <p class="title">程序员</p>
                    <p><span>简书</span> 收录了47489篇文章，1356636人关注</p>
                </div>
            </li>
            <li>
                <p>
                    <i class="fa fa-checked"></i>
                    已关注
                </p>
                <nuxt-link to="/" class="img">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="desc">
                    <p class="title">摄影</p>
                    <p><span>简书</span> 收录了47489篇文章，1356636人关注</p>
                </div>
            </li>
            <li>
                <p>
                    <i class="fa fa-checked"></i>
                    已关注
                </p>
                <nuxt-link to="/" class="img">
                    <img src="~/assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <div class="desc">
                    <p class="title">互联网</p>
                    <p><span>简书</span> 收录了47489篇文章，1356636人关注</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "followed"
    }
</script>

<style scoped>
    .followed ul li{
        padding-bottom: 20px;
        border-bottom: 1px solid #f5f5f5;
    }
    .followed ul li>p{
        float: right;
        margin-top: 8px;
        padding: 8px 0;
        width: 100px;
        font-size: 15px;
        border: 1px solid hsla(0,0%,59%,.6);
        background: none;
        border-radius: 40px;
        text-align: center;
    }
    .followed ul li .img img{
        width: 52px;
        height: 52px;
        margin-right: 8px;
        vertical-align: middle;
        display: inline-block;
        vertical-align: middle;
    }
    .followed ul li .desc{
        display: inline-block;
        margin-left: 10px;
        vertical-align: middle;
    }
    .followed ul li .desc>p:nth-of-type(2){
        font-size: 14px;
        margin-top: 4px;
    }
    .followed ul li .desc>p:nth-of-type(2)>span{
        color: cornflowerblue;
    }
</style>