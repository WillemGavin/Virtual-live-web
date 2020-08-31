<template>
<div class='personal'>
  <!-- <div class='headBar'>
    <div class='headText'>个人中心</div>
  </div> -->
  <div class='container'>
    <el-row class='tac'>
      <el-col :span="4">
        <el-menu
          :default-active="$route.path"
          router
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose">
          <el-menu-item index="myData">
            <i class='el-icon-user'></i>
            <span slot="title">个人资料</span>
          </el-menu-item>
          <el-menu-item index="memberCenter">
            <i class='el-icon-coin'></i>
            <span slot="title">会员中心</span>
          </el-menu-item>
          <el-menu-item index="myOrder">
            <i class='el-icon-s-order'></i>
            <span slot="title">我的订单</span>
          </el-menu-item>
          <el-menu-item index="myReceipt">
            <i class='el-icon-tickets'></i>
            <span slot="title">我的发票</span>
          </el-menu-item>
          <el-menu-item index="security">
            <i class='el-icon-first-aid-kit'></i>
            <span slot="title">安全中心</span>
          </el-menu-item>
        </el-menu>
      </el-col>
      <el-col :span="19" class='showText'>
        <router-view></router-view>
      </el-col>
    </el-row>
  </div>

</div>
  
</template>

<script>
export default {
  name: "personal",
  data(){
    return {
      
    }
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style lang='scss' scoped>
@import '@/common/style.scss';
.personal{
  background-color:rgb(245,247,249);
  box-sizing: border-box;
  display:flex;
  justify-content: space-between;
  flex-direction: column;
  align-items: center;
  // .headBar{
  //   width:100%;
  //   height:100px;
  //   padding:0 30px;
  //   display:flex;
  //   align-items: center;
  //   justify-content: center;
  //   box-sizing: border-box;
  //   .headText{
  //     height:100px;
  //     line-height:100px;
  //     height:100%;
  //     width:1200px;
  //     text-align: left;
  //     background-color: pink;
  //     padding:0 50px;
  //   }
  // }
  .container{
    margin:0 0 50px 0;
    background-color:white;
    width:1200px;
    padding:20px 0 0px 0;
    .tac{
      padding-bottom:20px;
      .el-col-4{
        margin-left:30px;
    }

    .el-menu{
      border-right:none;
    }
   .el-menu-item{
    font-size:18px;
    color:#7d7d7d;
  }
  .el-menu-item:focus, .el-menu-item:hover{
    background-color: $bg_orange !important;
    color:white;
    border-radius: 5px;
    i{
      color:white
    }
  }
  .showText{
    padding:0 20px;
    border-left:1px solid #ddd;
    margin-left:20px;
    background-color:white;
    height:500px;
  }
  }
 }
}

  
</style>
