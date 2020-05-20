<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>极派信息科技（苏州）有限公司</h3>
                    <p class=".text-justify">极派科技，总部位于苏州，主要从事产业互联网以及游戏产品的研发和系统集成。业务涉及物联网及大数据领域，助力企业客户完成工业4.0转型。</p>
                    <p class=".text-justify">极派科技作为创新型技术企业，公司法人于香港中文大学计算机系毕业并取得硕士学位。拥有一个高素质、技术精湛、年轻专业化、不断创新的研发团队，为公司蓬勃发展提供源源不断的活力与动力。核心团队成员来自于IBM，声网Agora，同程，蜗牛等一线互联网企业，在互联网产品的生产流程方面具有相当丰富的从业经验。</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{

        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 100px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

