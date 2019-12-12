<template>
  <div class="button-box">
    <input
      :style="style"
      :value="text"
      :class="size"
      type="button"
      class="button">
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
        return '确定';
      }
    },
    size: {
      type: String,
      default: () => {
        return '';
      }
    }
  },
  mounted() {},
  methods: {
    buttonClick() {
      console.log('click');
      this.$emit('click');
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../../style/default';
.button {
  height: 40px; /* 高度 */
  line-height: 40px; /* 高度 */
  border-width: 0; /* 边框宽度 */
  border-radius: 3px; /* 边框半径 */
  background: #1e90ff; /* 背景颜色 */
  cursor: pointer; /* 鼠标移入按钮范围时出现手势 */
  outline: none; /* 不显示轮廓线 */
  font-family: Microsoft YaHei; /* 设置字体 */
  color: white; /* 字体颜色 */
  padding: 0 10px;
  .large {
    font-size: 16px; /* 字体大小 */
    height: 50px; /* 高度 */
    line-height: 50px; /* 高度 */
    padding: 0 15px;
  }
}
</style>
