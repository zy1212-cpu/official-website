<template>
    <div id="NewsInformation">
        <div class="container">
            <div class="container text-center">
                <h3>新闻动态</h3>
                <p style="color:#b2b2b2">Company News</p>
            </div>
            <div class="nav container text-center">
                <a href="#" class="active">公司新闻</a>
                <a href="#">行业动态</a>
            </div>
            <ul class="news-container container-fuild">
                <li v-for="(item,index) in newsList" :key="index" class="wow fadeIn">
                    <div class="content">
                        <p>{{item.title}}</p>
                        <p>{{item.introduce}}</p>
                    </div>
                    <div class="time">
                        <p>{{item.date}}</p>
                        <span>{{item.year}}</span>
                    </div>
                    <div class="circle">
                        <img src="../assets/img/circle.png">
                        <i class="line center-block"></i>
                    </div>
                </li>
            </ul>
            <div class="contaianer-fuild text-center more">
                <i class="glyphicon glyphicon-th"></i>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'NewsInformation',
    data(){
        return{
            newsList:[
                {
                    id: '001',
                    title: '公司成立',
                    introduce: '极派科技，总部位于苏州，主要从事产业互联网以及游戏产品的研发和系统集成。业务涉及物联网及大数据领域，助力企业客户完成工业4.0转型',
                    date: '01-01',
                    year: '2018'
                },{
                    id: '002',
                    title: '至甄生活',
                    introduce: '本项目通过微信小程序的形式为家庭用户提供“保洁”，“家电维修”等家庭服务获取入口，方便家庭用户在线购买，预约和评价反馈',
                    date: '05-24',
                    year: '2018'
                },{
                    id: '003',
                    title: '安极能综合能源管理',
                    introduce: '本项目通过物联网技术完成配电房电力数据采集，并上传至云平台进行数据存储，监控预警和大数据分析。服务于学校，酒店，医院，工厂和企业园区等用电单位，提供用电安全保障的同时，尽可能实现能耗优化',
                    date: '01-01',
                    year: '2019'
                },{
                    id: '004',
                    title: '安极能app',
                    introduce: '本项目通过物联网技术完成配电房电力数据采集，并上传至云平台进行数据存储，监控预警和大数据分析。服务于学校，酒店，医院，工厂和企业园区等用电单位，提供用电安全保障的同时，尽可能实现能耗优化',
                    date: '05-24',
                    year: '2019'
                },{
                    id: '005',
                    title: '安易app',
                    introduce: '一款为电气服务从业的人员、团队，提供源源不断的售后项目订单APP。入驻安极能维保的工程师可在平台进行抢单来提高自己的收入。',
                    date: '04-01',
                    year: '2020'
                },{
                    id: '006',
                    title: '熔喷相关信息平台',
                    introduce: '用户发布分享企业的资源',
                    date: '05-01',
                    year: '2020'
                }
            ]
        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    },
}
</script>
<style scoped>
.nav{
    margin: 20px 0;
}
.nav>a{
    display: inline-block;
    text-decoration: none;
    width: 120px;
    height: 45px;
    line-height: 45px;
    color: #333;
    border: 1px solid #333;
}
.nav>a.active{
    color: #1e73be;
    border-color: #1e73be;
}
.nav>a:hover{
    color: #1e73be;
    border-color: #1e73be;
}
.news-container{
    overflow: hidden;
    margin-bottom: 0;
}
.news-container>li{
    width: 55.6%;
    height: 120px;
    float: left;
    color: #333;
    text-align: right;
    border-left: 1px solid transparent;
    border-right: 1px solid transparent;
}
.news-container>li:hover{
    color: #1e73be;
    border: 1px solid #1e73be;
    cursor: pointer;
}
.news-container>li:nth-of-type(2n){
    float: right;
    text-align: left;
}
.news-container>li>.content{
    width: 60%;
    float: left;
    padding: 20px 0;
}
.news-container>li>.time{
    width: 20%;
    float: left;
    padding: 10px 0;
}
.news-container>li>.time>p{
    font-size: 30px;
    margin: 5px 0;
}
.news-container>li>.circle{
    width: 20%;
    height: 100%;
    float: left;
    position: relative;
}
.news-container>li>.circle>img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    width: 20px;
    height: 20px;
}
.news-container>li>.circle>i{
    display: block;
    width: 1px;
    height: 100%;
    background: #707070;
}
.news-container>li:nth-of-type(2n)>.content{
    float: right;
}
.news-container>li:nth-of-type(2n)>.time{
    float: right;
}
.news-container>li:nth-of-type(2n)>.circle{
    float: right;
}
.news-container>li:nth-of-type(1)>.circle>i{
    height: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
}
.more{
    font-size: 25px;
    color: #707070;
}
.more>i{
    cursor: pointer;
}
@media screen and (max-width: 767px){
    .news-container>li{
        width: 100%;
    }
    .news-container>li>.content{
        width: 70%;
        text-align: left;
        float: right;
    }
    .news-container>li>.time{
        width: 30%;
        text-align: left;
        float: right;
    }
    .news-container>li>.circle{
        display: none;
    }
}
</style>

