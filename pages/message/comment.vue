<template>
    <div>
        <my-header></my-header>
        <div>
            <message></message>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    import message from '~/components/message'
    export default {
        name: "comment",
        components:{
            myHeader,
            message
        }
    }
</script>

<style scoped>

</style>