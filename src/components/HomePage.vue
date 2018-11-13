<template>
    <div>
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
      <template>
        <el-carousel indicator-position="outside" height="390px">
          <el-carousel-item v-for="item in pics" :key="item">
           <img width="100%" :src="item" />
          </el-carousel-item>
        </el-carousel>
      </template>
    </div>
</template>
<script>
export default {
  name: 'HomePage',
  data () {
    return {
      pics: ['../homepage/focus1.jpeg',
        '../homepage/focus2.jpeg']
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
</style>
