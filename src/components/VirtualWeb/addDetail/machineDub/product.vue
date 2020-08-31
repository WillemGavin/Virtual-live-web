<template>
<div class="product">
    <el-upload
    :class="{disabled:uploadDisabled}"
    :on-success="handleAvatarSuccess"
    :on-change="handleChange"
    :on-remove="handleRemove"
    action="#"
    limit=1
    list-type="picture-card"
    :auto-upload="false">
      <i slot="default" class="el-icon-plus"></i>
      <div slot="file" slot-scope="{file}">
        <img
          class="el-upload-list__item-thumbnail"
          :src="file.url" alt=""
        >
        <span class="el-upload-list__item-actions">
          <span
            class="el-upload-list__item-preview"
            @click="handlePictureCardPreview(file)"
          >
            <i class="el-icon-zoom-in"></i>
          </span>
          <span
            v-if="!disabled"
            class="el-upload-list__item-delete"
            @click="handleDownload(file)"
          >
            <i class="el-icon-download"></i>
          </span>
          <span
            v-if="!disabled"
            class="el-upload-list__item-delete"
            @click="handleRemove(file)"
          >
            <i class="el-icon-delete"></i>
          </span>
        </span>
      </div>
    </el-upload>
      <el-dialog :visible.sync="dialogVisible">
        <img width="100%" :src="dialogImageUrl" alt="">
      </el-dialog>

      <el-form ref="productForm" :model="productForm" label-width="80px">
        <el-form-item label="商品名称">
          <el-input type="text" v-model="productForm.proTitle"></el-input>
        </el-form-item>
        <el-form-item label="商品描述">
          <el-input type="textarea" v-model="productForm.proDescrition"></el-input>
        </el-form-item>
      </el-form>
    </div>

</template>
<script>
export default {
    data(){
        return{
          // 隐藏加号
          uploadDisabled:false,
          dialogVisible: false,
          addPicture:!this.dialogVisible,
          disabled: false,
          productForm:{
            proTitle:'',
            proDescrition:''
          }
        }
    },
    methods:{
      handleAvatarSuccess(res, file) {
        this.imageUrl = URL.createObjectURL(file.raw);
      },
      beforeAvatarUpload(file) {
        const isJPG = file.type === 'image/jpeg';
        const isLt2M = file.size / 1024 / 1024 < 2;

        if (!isJPG) {
          this.$message.error('上传头像图片只能是 JPG 格式!');
        }
        if (!isLt2M) {
          this.$message.error('上传头像图片大小不能超过 2MB!');
        }
        return isJPG && isLt2M;
      },
      handleChange(file,fileList){
        if(fileList.length >= 1){
          this.uploadDisabled = true;
        }
      },
       handleRemove(file) {
        console.log(file);
        this.fileList
        this.uploadDisabled = false
      },
      handlePictureCardPreview(file) {
        this.dialogImageUrl = file.url;
        this.dialogVisible = true;
      }
    }
}
</script>
<style lang="scss" scoped>
.product{
    width:100%;
    height:180px;
    display:flex;
    padding:10px 0;
    border-top: 2px dashed #ccc; 
    justify-content: space-evenly;
    align-items: center;
    box-sizing: border-box;
   .avatar-uploader{
     .el-upload {
        border: 1px dashed #d9d9d9;
        border-radius: 6px;
        cursor: pointer;
        position: relative;
        overflow: hidden;
      }
      .el-upload:hover {
        border-color: #409EFF;
      }
      .avatar-uploader-icon {
        font-size: 28px;
        color: #8c939d;
        width: 150px;
        height: 150px;
        line-height: 150px;
        text-align: center;
        border:2px dashed #d9d9d9

      }
      .avatar {
        width: 178px;
        height: 178px;
        display: block;
      }
    }
    .el-form-item:nth-child(2){
        margin-bottom: 0;
    }
  }
</style>