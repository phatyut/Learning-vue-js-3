<template>
    <div>
      <button @click="toggleHeight">Toggle Height</button>
      <div :style="{ width: dynamicHeight }" class="bg-red-500 h-[100px] w-[100px]"></div>
    </div>
  </template>
<script>
export default {
  data() {
    return {
      dynamicHeight: '100px'
    }
  },
  methods: {
    toggleHeight() {
      this.dynamicHeight = this.dynamicHeight === '100px' ? '100%' : '100px';
    }
  }
}
</script>
<style scoped>
div {
  transition: width 0.5s ease;
}
</style>
  