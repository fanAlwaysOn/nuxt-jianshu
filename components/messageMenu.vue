<template>
    <div>
        <ul>
            <li class="active">
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

    </div>
</template>

<script>
    export default {
        name: "message"
    }
</script>

<style scoped>
    .noticfication:before {
        content: '';
        display: table;
    }

    .noticfication .row {
        padding: 30px 0;
    }

    .noticfication .row .aside {
        position: fixed;
        top: 56px;
        bottom: 0;
        margin: 30px 0 0;
        padding: 0 0 30px;
        width: 280px;
        /*overflow: auto;*/
    }

    .noticfication .row .aside ul {
        margin: 0;
        padding: 0;
    }

    .noticfication .row .aside ul li {
        padding: 18px 22px;
        font-size: 16px;
    }

    .noticfication .row .aside ul li.active {
        background: #f5f5f5;
    }

    .noticfication .row .aside ul li:hover {
        background: #f5f5f5;
    }

    .noticfication .row .aside ul li i {
        margin-right: 19px;
        color: #EA6F5A;
        font-size: 20px;
        font-weight: 600;
    }
</style>