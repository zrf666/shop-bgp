<template>
   <div class="user-management">
     <el-card class="box-card">
       <el-row :gutter="20">
         <el-col :span="8">
           <el-input placeholder="请输入内容" v-model="searchData">
             <el-button slot="append" icon="el-icon-search" @click="onSearchBtnClick"></el-button>
           </el-input>
         </el-col>
         <el-col :span="6">
           <el-button class="add-btn" type="primary" @click="onAddUserBtnClick">添加用户</el-button>
         </el-col>
       </el-row>
       <el-table
           :data="tableData"
           stripe
           border
           style="width: 100%; margin: 20px 0">
         <el-table-column
             prop="id"
             label="唯一编号"
             width="180">
         </el-table-column>
         <el-table-column
             prop="account"
             label="账号"
             width="180">
         </el-table-column>
         <el-table-column
             prop="pwd"
             label="密码"
             width="180">
         </el-table-column>
           <el-table-column
               prop="phone"
               label="手机号">
           </el-table-column>
           <el-table-column
               prop="roleId"
               label="角色">
           </el-table-column>
           <el-table-column
               prop="type"
               label="状态">
           </el-table-column>
           <el-table-column
               fixed="right"
               label="操作">
             <template slot-scope="scope">
               <el-button @click="onUpdateUserInfoBtnClick(scope.row, scope.$index)" type="primary" plain size="small">修改</el-button>
               <el-button @click="onDeleteUserBtnClick(scope.row)" type="danger" plain size="small">删除</el-button>
             </template>
           </el-table-column>
       </el-table>
     </el-card>
   </div>
</template>

<script>
export default {
  name: "UserManagement",
  data(){
    return {
        searchData:'',
      tableData: [
            {
              id: '1',
              account: 'user1',
              pwd: '123456',
              phone:'18318787804',
              roleId:2,
              type:false,
              // totalNumber:
            }, {
              date: '2016-05-04',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1517 弄'
            }, {
              date: '2016-05-01',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1519 弄'
            }, {
              date: '2016-05-03',
              name: '王小虎',
              address: '上海市普陀区金沙江路 1516 弄'
          }
      ]
    }
  },

  methods:{
    onSearchBtnClick:function (){

    },
    //添加用户按钮的点击事件
    onAddUserBtnClick:function (){

    },
    onUpdateUserInfoBtnClick:function (row, index){

    },
    onDeleteUserBtnClick:function (row){

    }
  }
}
</script>

<style scoped>

</style>