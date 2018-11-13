<template>
    <div style="background-color: #e3e3e3;">
        <el-menu :default-active="activeIndex2" class="el-menu-demo" mode="horizontal" @select="handleSelect" background-color="#1a2b5e" text-color="#fff" active-text-color="#ffd04b">
            <el-menu-item index="1">首页</el-menu-item>
            <el-submenu index="2">
              <template slot="title">关于舒雨昂</template>
              <el-menu-item index="2-1">选项1</el-menu-item>
              <el-menu-item index="2-2">选项2</el-menu-item>
              <el-menu-item index="2-3">选项3</el-menu-item>
              <el-submenu index="2-4">
                <template slot="title">选项4</template>
                <el-menu-item index="2-4-1">选项1</el-menu-item>
                <el-menu-item index="2-4-2">选项2</el-menu-item>
                <el-menu-item index="2-4-3">选项3</el-menu-item>
              </el-submenu>
            </el-submenu>
            <el-menu-item index="3" >床垫产品</el-menu-item>
            <el-menu-item index="4">服务专区</el-menu-item>
            <el-menu-item index="5">加盟专区</el-menu-item>
            <el-menu-item index="6">舒雨昂专区</el-menu-item>
            <el-menu-item index="7">舒雨昂专题</el-menu-item>
            <el-menu-item index="8">舒雨昂商城</el-menu-item>
          </el-menu>
      <div style="padding: 50px;background-color: #1d2460">
      <template>
        <el-carousel indicator-position="outside" height="450px">
          <el-carousel-item v-for="item in pics" :key="item">
           <img width="100%" height="100%" :src="item" />
          </el-carousel-item>
        </el-carousel>
      </template>
      </div>
      <div style="padding-left: 150px;padding-right: 150px;">
        <div class="title">舒雨昂家具有限公司</div>
        <div class="line"></div>
        <div class="introduce">
        舒雨昂家具有限公司的总部，位于香港鸭脷洲海怡半岛第四座17楼D室。
        随着公司的发展于2004年在河南建立第一家大陆生产基地。公司占地24亩，
        厂房6000平方米，年产床垫10万张，热熔毡40万张，保温毡40万张，床布120万米。
        舒雨昂家具有限公司对材料的选材严格按照国家QB1952.2—2009标准来执行，
        全部材料都符合环保要求，采用当今最先进的生产工艺。以人为本，
        激发每一位员工的最大潜能，发扬团队精神，敢于自我挑战。销售的每一张床垫都有一个身份证，
        实行跟踪售后服务。 展望未来，舒雨昂家具有限公司与时俱进，走企业集团化，产品多元化的发展道路，
        不断开发新品、精品以最大的努力来满足消费者的需求。 舒雨昂，睡的香，愿舒雨昂床垫使你美梦成真！
        </div>
      </div>
      <div class="bottom">
      旗下系列
      </div>
    </div>
</template>
<script>
export default {
  name: 'HomePage',
  data () {
    return {
      pics: ['../static/homepage/focus1.jpeg',
        '../static/homepage/focus2.jpeg',
        '../static/homepage/focus3.png',
        '../static/homepage/focus4.png']
    }
  }
}
</script>

<style scoped>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
  .title{
    font-size: 38px;
    font-weight: bold;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  .introduce{
    line-height: 30px;font-size: 20px;width:80%;margin-top: 20px;margin-bottom: 20px;
  }
  .line{
    width: 50%;
    height: 1px;
    background-color: #666666;
  }
  .bottom{
    background-color: #1d2460;color: white;font-size: 30px; ;
  }
</style>
