<template>
<div class="weui-cells" :class="typeClass"><slot></slot></div>
</template>

<script>
export default {
  name: 'cells',
  props: {
    /**
     * Cells类型
     * access: 带跳转的列表项容器
     * form: 表单容器
     * radio: 单选列表项容器
     * checkbox: 多选列表项容器
     */
    type: {
      type: String,
      default: '',
      required: false
    }
  },
  
  computed: {
    typeClass() {
      return this.type ? `weui-cells_${this.type}` : '';
    }
  }
};
</script>
