<template>
    <div>
        <my-header></my-header>
        <div class="container watch">
            <div class="row">
                <!--左边侧边栏-->
                <div class="col-xs-offset-1 col-xs-7 aside" style="height: 400px;background: pink;">

                </div>
                <!--右方内容-->
                <div class="col-xs-16 main" style="height: 400px;background: orange;">

                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
        name: "watch",
        components:{
            myHeader
        }
    }
</script>

<style scoped>
    .watch{
        margin-top: 20px;
    }
</style>