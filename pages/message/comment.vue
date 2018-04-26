<template>
    <div>
        <my-header></my-header>
        <div class="container noticfication">
            <div class="row">
                <div class="col-xs-8 aside" style="height: 200px;background: pink">
                    <ul>
                        <li>
                            <nuxt-link to="/">
                                评论
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                简言
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                投稿请求
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to=""/>
                                喜欢和赞
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                关注
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                赞赏和付费
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                其它提醒
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <div class="col-xs-16 col-xs-offset-8 main" style="height: 400px;background: red"></div>
            </div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
        name: "comment",
        components:{
            myHeader
        }
    }
</script>

<style scoped>
    .noticfication:before{
        content: '';
        display: table;
    }
    .noticfication .row{
        padding: 30px 0;
    }
    .noticfication .row .aside{
        position: fixed;
        top: 56px;
        bottom: 0;
        margin: 30px 0 0;
        padding: 0 0 30px;
        width:280px;
        overflow: auto;
    }
</style>