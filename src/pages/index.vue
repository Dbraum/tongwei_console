<template>
  <el-data-table v-bind="tableConfig"></el-data-table>
</template>

<script>
export default {
  data() {
    return {
      tableConfig: {
        firstPage: 1,
        dataPath: 'payload.content',
        totalPath: 'payload.totalElements',
        hasDialog: true,
        hasPagination: true,
        hasOperation: true,
        isTree: false,
        url: '/user/api/v1/products',
        hasNew: true,
        hasEdit: true,
        hasView: false,
        hasDelete: true,
        single: false,
        extraButtons: [],
        columns: [
          {type: 'selection'},
          {prop: 'id', label: 'id'},
          {prop: 'name', label: '水果'},
          {prop: 'price', label: '价格'}
        ],
        searchForm: [
          {
            $type: 'input',
            $id: 'name',
            label: '水果',
            $el: {placeholder: '请输入'}
          }
        ],
        form: [
          {
            $type: 'input',
            $id: 'name',
            label: '水果',
            $el: {placeholder: '请输入'},
            rules: [{required: true, message: '请输入水果', trigger: 'blur'}]
          },
          {
            $type: 'input',
            $id: 'price',
            label: '价格',
            $el: {placeholder: '请输入'},
            rules: [{required: true, message: '请输入价格', trigger: 'blur'}]
          }
        ]
      }
    }
  },
  methods: {}
}
</script>
<style lang="less">
.index {
  .home-img {
    width: 100%;
  }
}
</style>
