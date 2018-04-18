<template>
    <div>登录</div>
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