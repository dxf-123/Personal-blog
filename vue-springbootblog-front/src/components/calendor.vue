<template>
  <div class="calendor">
    <div class="title">
      <!-- https://z3.ax1x.com/2021/08/31/hdu3a6.jpg -->
      <el-avatar src="https://z3.ax1x.com/2021/08/31/hdu3a6.jpg" ></el-avatar>
      <h4>博主信息</h4>
      <el-divider><i class="el-icon-user-solid"></i></el-divider>
    </div>
    <el-carousel indicator-position="outside">
      <el-carousel-item v-for="item in imgOptions" :key="item.id">
        <img :src="item.path" alt="图片" width="300px" />
      </el-carousel-item>
    </el-carousel>
    <div class="block">
      <h2 class="demonstration">对于博主的评级</h2>
      <el-rate v-model="value2" :colors="colors"> </el-rate>
    </div>
    <div class="message">
      <ul>
        <li>
          <el-tag type="success">
            <i class="el-icon-grape"></i>
            qq邮箱:2557523039@qq.com
          </el-tag>
        </li>
        <li>
          <el-tag type="warning">
            <i class="el-icon-ice-tea"></i>
            网易邮箱 qwxxhuchao@163.com
          </el-tag>
        </li>
        <li>
          <el-tag>
            <i class="el-icon-watermelon"></i>
            微信号:wxid_897c5xh9mya312
          </el-tag>
        </li>
        <li>
          <el-tag type="danger">
            <i class="el-icon-cherry"></i>
            电话：18864470086
          </el-tag>
        </li>
      </ul>
    </div>
    <div class="mine">
      <el-card class="box-card">
        <div slot="header" class="clearfix">
          <span>关于我</span>
        </div>
        <!-- v-for="o in 1" :key="o"  -->
        <div class="text item">
          如果没有奇迹，那就去创造！
        </div>
      </el-card>
    </div>
    <el-calendar v-model="value" width="300px" />
  </div>
</template>

<script>
export default {
  name: "calendor",
  data() {
    return {
      imgOptions: [
        {
          id: 1,
          path: "https://z3.ax1x.com/2021/08/31/hUk4S0.jpg",
        },
        {
          id: 2,
          path: "https://z3.ax1x.com/2021/08/31/hUkXf1.jpg",
        },
        {
          id: 3,
          path: "https://z3.ax1x.com/2021/08/31/hUkxl6.jpg",
        },
        {
          id: 4,
          path: "https://z3.ax1x.com/2021/08/31/hUASOO.jpg",
        },
        {
          id: 5,
          path: "https://z3.ax1x.com/2021/08/31/hUA9mD.jpg",
        },
        { 
         id: 6,
          path: "https://z3.ax1x.com/2021/08/31/hUAunS.jpg",
        },
        { 
         id: 7,
          path: "https://z3.ax1x.com/2021/08/31/hUAktA.jpg",
        }
      ],
      value: new Date(),
      value2: null,
      colors: ["#99A9BF", "#F7BA2A", "#FF9900"],
    };
  },
};
</script>

<style type="scss" scoped>

.calendor {
  display: flex;
  flex-direction: column;
  font-size: 14px;
}
.title{
  text-align: center;
  margin-top:10px;
}
.title .el-avatar{
  width:100px;
  height:100px;
}
.title /deep/ .el-avatar img{
  width: 100%;
  height: 100%;
}
.el-carousel{
  width:100%;
  margin:0px 0px 10px 0px;
}
.el-carousel img{
  /* width:250px; */
  height:180px;
}
 ::v-deep .el-carousel__container{
  height:200px;
}
.block {
  width: 210px;
  margin: 0 auto;
  text-align: center;
  background-color: rgb(220 169 31 / 29%);
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
}
.message {
  text-align:center;
}
/* .message ul {

} */
.message ul li {
  width: 210px;
  height: 32px;
  list-style: none;
  margin-top: 10px;
  margin-left: 70px;
  text-align: center;
  
  /* box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1) */
}
.message ul li .el-tag {
  width: 210px;
  height: 32px;
}
.mine{
  width: 210px;
  margin:0 auto;
}
.mine span{
  text-align: center;
  font-weight: 600;
  color: #58666e;
}
.text{
  text-align: center;
}
.el-calendar{
  margin-top:10px;
}
/deep/ .el-card {
    border: 1px solid #EBEEF5;
    background-color: #fafbfc;
    color: #909399;
    transition: .3s;
}
/deep/ .el-card__header {
    padding: 18px 20px;
    border-bottom: 1px solid #e6a23c;
    box-sizing: border-box;
    /* background: red; */
}
/deep/ .el-calendar__header {
    display: flex;
    justify-content: space-between;
    padding: 12px 20px;
    border-bottom: 1px solid #3a8ee6;
    background:#fdf6ec;
}
/deep/ .el-calendar__body {
    padding: 12px 20px 35px;
    background:#fdf6ec;
}

</style>