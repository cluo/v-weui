<template>
<a href="javascript:;" class="weui-btn" :class="[typeClass, disabled ? 'weui-btn_disabled' : '', mini ? 'weui-btn_mini' : '']">
  <slot></slot>
</a>
</template>

<script>
export default {
  name: 'button',
  props: {
    /**
     * 按钮颜色类型
     * primary: 主色
     * warn：警告色
     * default：默认色（灰色）
     */
    type: {
      type: String,
      default: 'primary',
      required: false
    },

    /**
     * 是否为disabled按钮，若为true则会阻止点击事件
     */
    disabled: {
      type: Boolean,
      default: false,
      required: false
    },

    /**
     * 是否为小按钮
     */
    mini: {
      type: Boolean,
      default: false,
      required: false
    },

    /**
     * 是否为plain按钮，plain按钮无填充色，只有边框
     * 目前只有primary和default类型支持plain按钮
     */
    plain: {
      type: Boolean,
      default: false,
      required: false
    }
  },

  computed: {
    typeClass() {
      return `weui-btn${this.plain ? '_plain' : ''}_${this.type}`;
    }
  }
}
</script>
