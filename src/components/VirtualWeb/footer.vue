<template>
  <div class='footer'>
    <div class="footerContainer">
      <div class="footerLeft">
        <div class='linkList'>
          <el-link :underline='false' type='info' href='javascript;'>联系我们</el-link>
          <el-link :underline='false' type='info' href='javascript;'>使用协议</el-link>
          <el-link :underline='false' type='info' href='javascript;'>信息中心</el-link>

        </div>
        <span>Copyright © 2018-2020 xxx有限公司版权所有</span>
      </div>
      <div class="footerRight">
        <img class='QRCode' :src="QRCode" alt="" >
        <span>微信扫一扫 使用小程序</span>
      </div>
    </div>
    <span class="authority">
      <img class='policeIcon' :src="policeIcon" alt="">
            <span>皖ICP备88888888号</span>
    </span>
  </div>

</template>
<script>
export default {
  data(){
    return {
      QRCode:require('@/assets/VirtualWeb/footerBar/img/QRCode.jpg'),
      policeIcon:require('@/assets/VirtualWeb/footerBar/img/policeIcon.jpg')

    }

  }

}
</script>
<style scoped lang='scss'>
//@import  '@/common/reset.css';
//@import '@/common/style.scss';
.footer{
  width:100%;
  height:240px;
  font-size: 13px;
  color:#7d7d7d;
  display:flex;
  justify-content: space-around;
  flex-direction: column;
  align-items: center;
  // background-color: $light-orange;
  /* letter-spacing: 1px; */
}
.footerContainer{
  // background-color: $light-orange;
  width:100%;
  height:100%;
  padding: 10px 40px;
  display:flex;
  justify-content: space-around;
  align-items: center;
  border-top:1px  solid #ccc;
  border-bottom:1px  solid #ccc

}
.footerLeft{
  display:flex;
  justify-content: space-around;
  flex-direction: column;
  align-items: flex-start;

}
.linkList{
  width:100%;
  display:flex;
  justify-content: space-between;
  align-items: center;
  margin:20px 0;

}
.footerRight{
  display:flex;
  justify-content: space-around;
  flex-direction: column;
  align-items: center;
}
.QRCode{
  width:50px;
  height:50px;
}
.authority{
  margin:20px 0;
  display:flex;
  justify-content: space-between;
  align-items: center;

}
.policeIcon{
  margin:0 5px
}

</style>
<script>
export default {
  data(){
    return{
      QRCode: require('@/assets/VirtualWeb/footerBar/img/QRCode.jpg'),
      policeIcon:require('@/assets/VirtualWeb/footerBar/img/policeIcon.jpg')
    }
  }
}
</script>
