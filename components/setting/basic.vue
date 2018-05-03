<template>
    <div class="basic">
        <table>
            <tbody>
            <tr>
                <td class="top-line">
                    <nuxt-link to="/">
                        <img src="~/assets/img/default-avatar.jpg" alt="">
                    </nuxt-link>
                </td>
                <td class="btn">
                    <a href="javascript(0)">
                        <input type="file" class="hide" unselectable="on">
                        更改头像
                    </a>
                </td>
            </tr>
            <tr>
                <td>昵称</td>
                <td>
                    <input class="nickname" type="text" placeholder="吹吹">
                </td>
            </tr>
            <tr>
                <td>电子邮件</td>
                <td class="bind"><span>点击绑定</span></td>
            </tr>
            <tr>
                <td>手机</td>
                <td>
                    131****2213&nbsp;
                    <span class="phone"><i class="fa fa-check"></i>已验证</span>
                </td>
            </tr>
            <tr>
                <td>语言设置</td>
                <td>
                    <div class="col-xs-8">
                        <input type="radio" checked id="simple" name="lang"><label for="simple">中文简体</label>
                    </div>
                    <div class="col-xs-16">
                        <input type="radio" id="complex" name="lang"><label for="complex">中文繁体</label>
                    </div>
                </td>
            </tr>
            <tr>
                <td>接收谁的简信</td>
                <td>
                    <div class="col-xs-8">
                        <input type="radio" name="receive" checked id="all"><label for="all">所有人</label>
                    </div>
                    <div class="col-xs-16">
                        <input type="radio" name="receive" id="followed"><label for="followed">我关注的人、我发过简信的人</label>
                    </div>
                </td>
            </tr>
            <tr>
                <td>提醒邮件通知</td>
                <td>
                    <div class="col-xs-8">
                        <input type="radio" name="tell" checked id="dynanic"><label for="dynanic">所有动态</label>
                    </div>
                    <div class="col-xs-11">
                        <input type="radio" name="tell" id="unRead"><label for="unRead">每天未读汇总<i class="fa fa-"></i></label>
                    </div>
                    <div class="col-xs-5">
                        <input type="radio" name="tell" id="noReceive"><label for="noReceive">不接收<i class="fa fa-"></i></label>
                    </div>
                </td>
            </tr>
            </tbody>
        </table>
        <input class="save" type="submit" value="保存">
    </div>
</template>

<script>
    export default {
        name: "basic"
    }
</script>

<style scoped>
    .basic table{
        width: 100%;
        padding: 20px 0;
        border-collapse:collapse;
    }
    .basic table tr{
        width: 100%;
    }
    .basic table tr td{
        font-size: 14px;
    }
    .basic table tr>td:nth-of-type(1){
        width: 23%;
    }
    .basic table tr>td:nth-of-type(2){
        width: 70%;
    }
    .basic table tr .top-line a img{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        vertical-align: middle;
    }
    .basic table tr .btn{
        vertical-align: middle;
    }
    .basic table tr .btn a{
        font-size: 14px;
        border: 1px solid rgba(59,194,29,.7);
        color: #42c02e!important;
        padding: 7px 12px;
        margin-bottom: 0;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        cursor: pointer;
        border-radius: 15px;
    }
    .basic table tr .btn .hide{
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }
    .basic table tr:nth-of-type(n+2){
        border-bottom: 1px solid #f0f0f0;
    }
    .basic table tr:nth-of-type(n+2)>td{
        padding: 20px 0;
    }
    .basic table tr td .nickname{
        padding: 5px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
    }
    .basic table tr td.bind span{
        border: 1px solid #42c02e;
        color: #42c02e!important;
        background-color: rgba(59,194,29,.05);
        font-size: 14px;
        padding: 6px 15px;
        font-size: 12px;
        font-weight: 400;
        line-height: normal;
        border-radius: 40px;
        background: none;
    }
    .basic table tr td .phone{
        color: gray;
    }
    .basic table tr td>div{
        padding: 0;
    }
    .basic .save{
        width: 100px;
        margin: 30px 0 60px;
        padding: 7px 12px;
        border: none;
        display: inline-block;
        margin-bottom: 0;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        border-radius: 40px;
        color: #fff;
        background-color: #42c02e;
        border-color: #42c02e;
    }
</style>