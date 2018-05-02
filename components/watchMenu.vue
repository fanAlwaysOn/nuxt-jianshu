<template>
    <div>
        <div class="watch-watch">
            <p>
                全部关注
                <i class="fa fa-caret-square-o-down"></i>
            </p>
            <p>
                <i class="fa fa-user-plus"></i>
                添加关注
            </p>
        </div>
        <div class="watch-list">
            <ul>
                <li @click="leftMenu='jianyou'" @mouseenter="leftMenu='jianyou'"
                    :class="leftMenu=='jianyou'?'active':''">
                    <nuxt-link to="/watch/watch">
                        <img src="~/assets/img/default-avatar.jpg" alt="">
                        <span>简友圈</span>
                    </nuxt-link>
                </li>
                <li @click="leftMenu='yuluo'" @mouseenter="leftMenu='yuluo'"
                    :class="leftMenu=='yuluo'?'active':''">
                    <nuxt-link to="/watch/watch-user-yuluo">
                        <img src="~/assets/img/default-avatar.jpg" alt="">
                        <span>雨落黄岩</span>
                    </nuxt-link>
                </li>
                <li @click="leftMenu='hebo'" @mouseenter="leftMenu='hebo'"
                    :class="leftMenu=='hebo'?'active':''">
                    <nuxt-link to="/watch/watch-user-hebo">
                        <img src="~/assets/img/default-avatar.jpg" alt="">
                        <span>河伯爷爷</span>
                    </nuxt-link>
                </li>
                <li @click="leftMenu='woshi'" @mouseenter="leftMenu='woshi'"
                    :class="leftMenu=='woshi'?'active':''">
                    <nuxt-link to="/watch/watch-user-woshi">
                        <img src="~/assets/img/default-avatar.jpg" alt="">
                        <span>我是谁</span>
                    </nuxt-link>
                </li>
            </ul>
        </div>
        <ul></ul>
    </div>
</template>

<script>
    export default {
        name: "watchMenu",
        data() {
            return {
                leftMenu: 'jianyou',
            }
        }
    }
</script>

<style scoped>
    .watch {
        margin-top: 20px;
    }

    .watch .row .aside {
        padding: 5px 0;
    }

    .watch .row .aside .watch-watch {
        padding: 0 5px;
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-between;
        margin-bottom: 10px;
    }

    .watch .row .aside .watch-watch p {
        font-size: 14px;
    }

    .watch .row .aside .watch-watch p:nth-of-type(1) {
        font-size: 15px;
    }

    .watch .row .aside .watch-list ul {
        margin: 0;
    }

    .watch .row .aside .watch-list ul li {
        padding: 10px 8px;
    }

    .watch .row .aside .watch-list ul li.active {
        background: #f5f5f5;
    }

    .watch .row .aside .watch-list ul li img {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        margin-right: 10px;
        vertical-align: middle;
    }

    .watch .row .aside .watch-list ul li span {
        font-size: 15px;
        vertical-align: middle;
    }
    .watch .row .main{
        padding: 0;
    }
</style>