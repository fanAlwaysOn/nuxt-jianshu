<template>
    <div class="personal">
        <table>
            <tbody>
                <tr>
                    <td>性别</td>
                    <td>
                        <div class="col-xs-6">
                            <input type="radio" checked name="sex" id="male"><label for="male">男</label>
                        </div>
                        <div class="col-xs-6">
                            <input type="radio" name="sex" id="female"><label for="female">女</label>
                        </div>
                        <div class="col-xs-6">
                            <input type="radio" name="sex" id="hidden"><label for="hidden">保密</label>
                        </div>
                    </td>
                </tr>
                <tr class="intro">
                    <td>个人简介</td>
                    <td>
                        <textarea placeholder="填写你的个人简介"></textarea>
                    </td>
                </tr>
                <tr class="web">
                    <td>个人网站</td>
                    <td>
                        <input placeholder="http://你的网站"></input>
                        <p>填写后会在个人主页显示图标</p>
                    </td>
                </tr>
                <tr class="frcode">
                    <td>微信二维码</td>
                    <td>
                        <input type="file" class="hidden">
                        <a href="">
                            <input type="file" class="hidden">
                            更换图片
                        </a>
                        <p>上传后会在个人主页显示图标</p>
                    </td>
                </tr>
                <tr class="share">
                    <td>社交账号</td>
                    <td>
                        <p>你可以通过绑定的社交帐号登录简书。出于安全因素, 你最初用来创建账户的社交帐号不能移除。</p>
                        <p>如果帐号被占用，你可以在简书帐号绑定解绑相关问题汇总中获得相关帮助。</p>
                        <ul>
                            <li>
                                <i class="fa fa-weibo" style="color: #ea6f5a"></i>
                                绑定到微博
                                <i class="fa fa-angle-right"></i>
                            </li>
                            <li>
                                <i class="fa fa-weixin" style="color: orangered"></i>
                                绑定到微信
                                <i class="fa fa-angle-right"></i>
                            </li>
                            <li>
                                <i class="fa fa-qq" style="color: blue"></i>
                                绑定到QQ
                                <i class="fa fa-angle-right"></i>
                            </li>
                            <li>
                                <i class="fa fa-twitter" style="color: #00bb29"></i>
                                绑定到豆瓣
                                <i class="fa fa-angle-right"></i>
                            </li>
                            <li>
                                <i class="fa fa-google" style="color: #3db922"></i>
                                绑定到Google
                                <i class="fa fa-angle-right"></i>
                            </li>
                        </ul>
                    </td>
                </tr>
            </tbody>
        </table>
        <input class="save" type="submit" value="保存">
    </div>
</template>

<script>
    export default {
        name: "personal"
    }
</script>

<style scoped>
    .personal table{
        width: 100%;
        padding: 20px 0;
        border-collapse:collapse;
    }
    .personal table tr{
        width: 100%;
    }
    .personal table tr td{
        font-size: 14px;
        padding: 15px 0;
        border-bottom: 1px solid #f5f5f5;
    }
    .personal table tr>td:nth-of-type(1){
        width: 23%;
    }
    .personal table tr>td:nth-of-type(2){
        width: 70%;
    }
    .personal table tr.intro textarea{
        width: 100%;
        height: 100px;
        margin-bottom: 10px;
        padding: 8px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
        display: block;
        resize: none;
        outline-style: none;
    }
    .personal table tr.web input{
        width: 100%;
        margin-bottom: 10px;
        padding: 5px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
    }
    .personal table tr.web p{
        text-align: right;
        color: gray;
        font-size: 12px;
    }
    .personal table tr.frcode>td>input{
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }
    .personal table tr.frcode>td>a{
        padding: 7px 15px;
        font-size: 12px;
        font-weight: 400;
        line-height: normal;
        border-radius: 40px;
        background: none;
        display: inline-block;
        margin-bottom: 10px;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        border: 1px solid rgba(59,194,29,.7);
        color: #42c02e!important;
    }
    .personal table tr.frcode>td>a>input{
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }
    .personal table tr.frcode p{
        text-align: right;
        color: gray;
        font-size: 12px;
    }
    .personal table tr.share p{
        text-align: left;
        color: gray;
        font-size: 12px;
        margin-bottom: 8px;
    }
    .personal table tr.share ul{
        margin: 0;
    }
    .personal table tr.share ul li{
        margin: 0;
        font-size: 16px;
        padding: 20px 0;
        border-bottom: 1px solid #f5f5f5;
    }
    .personal table tr.share ul li:nth-last-of-type(1){
        border: none;
    }
    .personal table tr.share ul li i:nth-of-type(1){
        margin-right: 15px;
    }
    .personal .save{
        width: 100px;
        margin: 30px 0 60px;
        padding: 7px 12px;
        border: none;
        display: inline-block;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        border-radius: 40px;
        color: #fff;
        background-color: #42c02e;
        border-color: #42c02e;
    }
</style>