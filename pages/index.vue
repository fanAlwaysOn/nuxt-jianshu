<template>
    <div>
        <my-header></my-header>
        <div class="container index">
            <div class="row">
                <div class="col-xs-16 main">
                    <!--热门专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c1.jpg" alt="">
                            <span class="name">手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c2.jpg" alt="">
                            <span class="name">读书</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c3.jpg" alt="">
                            <span class="name">社会热点</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c4.jpg" alt="">
                            <span class="name">@IT·互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c5.png" alt="">
                            <span name="name">旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c6.jpg" alt="">
                            <span name="name">历史</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="collection">
                            <img src="~/assets/img/c7.jpg" alt="">
                            <span name="name">自然科普</span>
                        </nuxt-link>
                        <nuxt-link to="/" class="more-collection">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div class="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <div class="">
                                    <nuxt-link to="/" class="wrap-img">
                                        <img src="~assets/img/note.jpg" alt="">
                                    </nuxt-link>
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                            <span>
                                                <i class="fa fa-money"></i>
                                                10
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="">
                                    <!--<nuxt-link to="/">-->
                                        <!--<img src="~assets/img/note.jpg" alt="">-->
                                    <!--</nuxt-link>-->
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <div class="">
                                    <nuxt-link to="/" class="wrap-img">
                                        <img src="~assets/img/note.jpg" alt="">
                                    </nuxt-link>
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                            <span>
                                                <i class="fa fa-money"></i>
                                                10
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="">
                                    <!--<nuxt-link to="/">-->
                                    <!--<img src="~assets/img/note.jpg" alt="">-->
                                    <!--</nuxt-link>-->
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <div class="">
                                    <nuxt-link to="/" class="wrap-img">
                                        <img src="~assets/img/note.jpg" alt="">
                                    </nuxt-link>
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                            <span>
                                                <i class="fa fa-money"></i>
                                                10
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="">
                                    <!--<nuxt-link to="/">-->
                                    <!--<img src="~assets/img/note.jpg" alt="">-->
                                    <!--</nuxt-link>-->
                                    <div class="content">
                                        <div class="author">
                                            <nuxt-link to="/" class="avatar">
                                                <img src="~assets/img/default-avatar.jpg" alt="">
                                            </nuxt-link>
                                            <div class="info">
                                                <nuxt-link to="/" class="nickname">
                                                    测试用户
                                                </nuxt-link>
                                                <span class="time">04.12 10:18</span>
                                            </div>
                                        </div>
                                        <nuxt-link class="title" to="">从《唐人街探案2》探寻一个屌丝逆袭的真相</nuxt-link>
                                        <div class="abstruct">《唐人街探案2》目前票房已经突破33亿，是2015年《唐人街探案1》8亿余票房的4倍多，票房收入高居历年国产喜剧电影的榜首。这部电影成功的背后，秦风的扮演者刘昊然，宋义的扮演...</div>
                                        <div class="meta">
                                            <nuxt-link to="/" class="collection-tag">社会与法</nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-eye"></i>
                                                1500
                                            </nuxt-link>
                                            <nuxt-link to="/">
                                                <i class="fa fa-comment"></i>
                                                100
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i>
                                                20
                                            </span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <a href="" class="load-more"> 阅读更多</a>
                </div>
                <!--侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside">
                    <div class="row">
                        <!--广告-->
                        <div class="board">
                            <nuxt-link to="/">
                                <img src="~/assets/img/aside1.png" alt="">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/aside2.png" alt="">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/aside3.png" alt="">
                            </nuxt-link>
                            <nuxt-link to="/">
                                <img src="~/assets/img/aside4.png" alt="">
                            </nuxt-link>
                        </div>
                        <!--推荐作者-->
                        <div class="recommended-authors">
                            <div class="title">
                                <span>推荐作者</span>
                                <nuxt-link to="" class="page-change">
                                    <i class="fa fa-refresh"></i>换一批
                                </nuxt-link>
                            </div>
                            <ul class="recommended-list">
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                                <li>
                                    <nuxt-link class="avatar" to="/">
                                        <img src="~assets/img/default-avatar.jpg" alt="">
                                    </nuxt-link>
                                    <a href="" class="follow">
                                        <i class="fa fa-plus"></i> 关注
                                    </a>
                                    <nuxt-link to="/" class="name">简书用户</nuxt-link>
                                    <p>写了1958k字，1.9k喜欢</p>
                                </li>
                            </ul>
                            <nuxt-link to="" class="find-more">
                                查看更多 <i class="fa fa-angle-right"></i>
                            </nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
import myHeader from "../components/myHeader.vue"
    export default {
        head:{
            title:"简书-创作你的创作",
            meta:[
                {chartset:"utf-8"},
                {name:"keywords",content:"简书首页"},
                {name:"description",content:"简书首页"},
                {name:"author",content:"范瑞"},
            ]
        },
        components:{
            myHeader
        },
        data () {
            return {
                name:'首页'
            }
        }
    }
</script>
<style>

</style>