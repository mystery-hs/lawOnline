<template>

    <el-container>
      <el-header class="el-header" style="font-size: 12px">
        <el-row :gutter="10">
          <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1">
            <div class="grid-content bg-purple">
              <lable class="size">合作伙伴信息管理</lable>
            </div>
          </el-col>

          <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple-light">
            <el-dropdown style="text-align: right">
              <i class="el-icon-setting" ></i>
              <el-dropdown-menu slot="dropdown">
                <el-dropdown-item>查看1</el-dropdown-item>
                <el-dropdown-item>新增</el-dropdown-item>
                <el-dropdown-item>删除</el-dropdown-item>
              </el-dropdown-menu>
            </el-dropdown>
          </div></el-col>

        </el-row>


      </el-header>

      <el-main>
        <el-table :data="tableData">
          <el-table-column prop="id" label="编号" width="140">
          </el-table-column>
          <el-table-column prop="name" label="姓名" width="120">
          </el-table-column>
          <el-table-column prop="address" label="地址">
          </el-table-column>
          <el-table-column prop="number" label="联系方式">
          </el-table-column>
          <el-table-column prop="data" label="处理事务">
          </el-table-column>
        </el-table>
      </el-main>
    </el-container>

</template>

<style>

.el-header{
  background-color: #B3C0D1;
  color: #333;
  line-height: 60px;
}
.size{
  color: #909399;
  font-weight: 500;
  font-weight: bold;
  font-size:small;
}


</style>

<script>
export default {
  data() {
    const item = {
      id: 12138,
      name: '王小虎',
      address: '上海市普陀区金沙江路 1518 号',
      number:'12345',
      data:'法律赔偿'

    };
    return {
      tableData: Array(5).fill(item)
    }
  }
};
</script>