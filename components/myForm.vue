<template>
    <div>
        <form method="post" class="new-comment">
            <slot></slot>
            <textarea name="comment-content" placeholder="写下你的评论"></textarea>
            <div class="write-function-block">
                <div class="emoji-modal-wrap">
                    <a class="emoji" @click="showEmojiFn()">
                        <i class="fa fa-smile-o"></i>
                    </a>
                    <transition name="fade">
                        <div class="emoji-modal" v-show="showEmoji">
                            <vue-emoji @select="selectEmoji">
                            </vue-emoji>
                            <span class="pop-arrow arrow"></span>
                        </div>
                    </transition>
                </div>
                <div class="hint">Ctrl+Enter发表</div>
                <a href="#" class="btn-send">发送</a>
                <a href="#" class="btn-cancel">取消</a>
            </div>
        </form>
    </div>
</template>

<script>
    import data from '../plugins/emoji-data.js'
    import vueEmoji from './emoji'
    export default {
        name: "myForm",
        components:{
            vueEmoji
        },
        data(){
            return{
                showEmoji:false,
                data1:data,
                data:[],
                vlaue:''
            }
        },
        methods:{
            showEmojiFn:function () {
                this.showEmoji = !this.showEmoji;
                console.log(this.data1)
            },
            selectEmoji:function (code) {
                this.showEmoji = false;
                this.value += code;
            },
            submit () {
                this.data.push(this.value);
                this.value = ''
            }
        }
    }
</script>

<style scoped>
    .fade-enter-active, .fade-leave-active { transition: opacity .5s; }
    .fade-enter, .fade-leave-active { opacity: 0; }
    .fade-move { transition: transform .4s; }

    .list-enter-active, .list-leave-active { transition: all .5s; }
    .list-enter, .list-leave-active { opacity: 0; transform: translateX(30px); }
    .list-leave-active { position: absolute !important; }
    .list-move { transition: all .5s;}
</style>