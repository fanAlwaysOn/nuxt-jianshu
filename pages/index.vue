<template>
    <div>
        <my-header></my-header>
        <p style="height: 300px;background: pink">主体内容</p>

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