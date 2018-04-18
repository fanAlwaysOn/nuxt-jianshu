<template>
    <div>注册</div>
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