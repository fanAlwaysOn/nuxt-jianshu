<template>
    <div>
        <ul>
            <li :class="whichList=='comment'?'active':''" @click="whichList='comment'">
                <nuxt-link to="/message/comment">
                    <i class="fa fa-comment-o"></i>
                    评论
                </nuxt-link>
            </li>
            <li :class="whichList=='chats'?'active':''" @click="whichList='chats'">
                <nuxt-link to="/message/chats">
                    <i class="fa fa-envelope-o"></i>
                    简讯
                </nuxt-link>
                <span>1</span>
            </li>
            <li :class="whichList=='watch'?'active':''" @click="whichList='watch'">
                <nuxt-link to="/message/follows">
                    <i class="fa fa-plus-square-o"></i>
                    关注
                </nuxt-link>
            </li>
            <li :class="whichList=='like'?'active':''" @click="whichList='like'">
                <nuxt-link to="/message/likes">
                    <i class="fa fa-heart-o"></i>
                    喜欢和赞
                </nuxt-link>
            </li>
            <li :class="whichList=='other'?'active':''" @click="whichList='other'">
                <nuxt-link to="/message/others">
                    <i class="fa fa-ellipsis-h"></i>
                    其它提醒
                </nuxt-link>
            </li>
        </ul>

    </div>
</template>

<script>
    export default {
        name: "message",
        props:["title"],
        data(){
            return{
                whichList:'comment'
            }
        },
        mounted:function () {
            this.whichList = this.title;
        }
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
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-between;
    }
    .noticfication .row .aside ul li>span{
        margin-right: 12px;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: #ea6f5a;
        color: #fff;
        text-align: center;
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