<template>
    <div class="comment-list">
        <form method="post" class="new-comment">
            <nuxt-link to="/u/123" class="avatar">
                <img src="~/assets/img/default-avatar.jpg" alt="">
            </nuxt-link>
            <textare name="comment-content" placeholder="写下你的评论"></textare>
            <div class="write-function-block">
                <div class="emoji-modal-wrap">
                    <a href="#" class="emoji">
                        <i class="fa fa-smile-o"></i>
                    </a>
                    <div class="emoji-modal"></div>
                </div>
                <div class="hint">Ctrl+Enter发表</div>
                <a href="#" class="btn-send">发送</a>
                <a href="#" class="btn-cancel">取消</a>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        name: "myComment",
        data(){
            return{

            }
        }
    }
</script>

<style scoped>

</style>