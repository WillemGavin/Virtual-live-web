<template>
<div class='myData'>
<<<<<<< HEAD
    <div class="pageTitle">个人资料</div>
     <div class="signupBar">
        <el-form id='el-form' ref="personalForm"   :model="signupForm" label-width="100px" :rules="rules" class="demo-ruleForm">
            <el-form-item  prop="tel" label="登录账号">
                <!-- 登录账号即手机密码 -->
                <el-input v-model="personalForm.tel" placeholder="登录账号" autocomplete="off" readonly></el-input>
            </el-form-item>
            <el-form-item  prop="email" label="邮箱">
                <el-input type="text" v-model="personalForm.email" placeholder="邮箱账号" autocomplete="off"></el-input>
            </el-form-item>
            <el-form-item label="从事行业" prop="job">
                <el-select v-model="personalForm.job" placeholder="请选择" autocomplete="off">
                    <el-option label="电商" value="dianshang"></el-option>
                    <el-option label="广告" value="guanggao"></el-option>
                    <el-option label="其他" value="qita"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item  prop="enterprise" label="公司名称">
                <el-input type="text" v-model="personalForm.enterprise" placeholder="公司名称" autocomplete="off"></el-input>
            </el-form-item>
            
            <el-form-item>
                <el-button type="primary" @click="saveForm()">保存</el-button>
            </el-form-item>
        </el-form>
    </div>
=======
  sdfsdafasdfas
<!--    <div class="pageTitle">个人资料</div>-->
<!--     <div class="signupBar">-->
<!--        <el-form id='el-form' ref="personalForm"   :model="signupForm" label-width="100px" :rules="rules" class="demo-ruleForm">-->
<!--            <el-form-item  prop="tel" label="登录账号">-->
<!--                &lt;!&ndash; 登录账号即手机密码 &ndash;&gt;-->
<!--                <el-input v-model="personalForm.tel" placeholder="登录账号" autocomplete="off" readonly></el-input>-->
<!--            </el-form-item>-->
<!--            <el-form-item  prop="email" label="邮箱">-->
<!--                <el-input type="text" v-model="personalForm.email" placeholder="邮箱账号" autocomplete="off"></el-input>-->
<!--            </el-form-item>-->
<!--            <el-form-item label="从事行业" prop="job">-->
<!--                <el-select v-model="personalForm.job" placeholder="请选择" autocomplete="off">-->
<!--                    <el-option label="电商" value="dianshang"></el-option>-->
<!--                    <el-option label="广告" value="guanggao"></el-option>-->
<!--                    <el-option label="其他" value="qita"></el-option>-->
<!--                </el-select>-->
<!--            </el-form-item>-->
<!--            <el-form-item  prop="enterprise" label="公司名称">-->
<!--                <el-input type="text" v-model="personalForm.enterprise" placeholder="公司名称" autocomplete="off"></el-input>-->
<!--            </el-form-item>-->

<!--            <el-form-item>-->
<!--                <el-button type="primary" @click="saveForm()">保存</el-button>-->
<!--            </el-form-item>-->
<!--        </el-form>-->
<!--    </div>-->
>>>>>>> f25931a03284d65882e8cfa9176a9c3795f80f4c
</div>
</template>
<script>
export default {
    data(){
        return{
            readonly: true,
            personalForm: {
                // 提取登录信息
                tel:'',
                emai:'',
                job:'',
                enterprise:''
            },
            rules: {
<<<<<<< HEAD
               
=======

>>>>>>> f25931a03284d65882e8cfa9176a9c3795f80f4c

            }
        }
    },
     methods:{
        getconfirmCode(){
            console.log('getconfirmCode')
        },
        saveForm(){
            // 提交表单
            console.log('提交成功!')
<<<<<<< HEAD
        
        },
        
=======

        },

>>>>>>> f25931a03284d65882e8cfa9176a9c3795f80f4c
    }
}
</script>
<style lang="scss" scoped>
@import '@/common/style.scss';
.myData{
    display:flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    .pageTitle{
        @include pageTitle
    }
    .signupBar{
        width:100%;
        display:flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        padding-top:50px;
        #el-form{
            width:400px;
            .el-select{
                width:100%;
            }
        }
        & ::v-deep .el-button--primary{
            width:100%;
            background-color: $bg-orange;
            border-color:$bg-orange
        }
        &::v-deep .el-form-item__label{
            float:left;
        }
    }
}
<<<<<<< HEAD
     
</style>
=======

</style>
>>>>>>> f25931a03284d65882e8cfa9176a9c3795f80f4c
