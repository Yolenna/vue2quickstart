<template>
  <el-table
    :data="tableData"
    selection-mode="multiple"
    @selectionchange="handleSelectionChange"
    style="width: 100%">
    <el-table-column
      type="selection"
      width="50">
    </el-table-column>
    <el-table-column
      type="index"
      width="50">
    </el-table-column>
    <el-table-column
      property="date"
      label="日期"
      width="120">
    </el-table-column>
    <el-table-column
      property="name"
      label="姓名"
      width="120">
    </el-table-column>
    <el-table-column
      property="address"
      label="地址">
    </el-table-column>
  </el-table>
</template>

<script type="text/ecmascript-6">
  import {Table, TableColumn, Tooltip, Checkbox} from 'element-ui'

  export default {

    data() {
      return {
        tableData: [],
        singleSelection: {}
      }
    },
    mounted(){
      this.tableData = [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
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
      }]
    },
    methods: {
      handleSelectionChange(val) {
        this.singleSelection = val;
      }
    }
  }
</script>
