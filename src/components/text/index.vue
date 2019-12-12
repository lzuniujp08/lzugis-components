<template>
  <div class="button-box">
    <label
      :style="style"
      class="text">
      {{ text }}
    </label>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    style: {
      type: Object,
      default: () => {
        return {};
      }
    },
    text: {
      type: String,
      default: () => {
        return '文本';
      }
    }
  },
  mounted() {},
  methods: {}
};
</script>

<style lang="scss" scoped>
@import '../../style/default';
.text {
  font-family: Microsoft YaHei; /* 设置字体 */
  color: white; /* 字体颜色 */
}
</style>
