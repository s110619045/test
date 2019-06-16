<template>
<div class="container">
  <div v-for="index in 16" :key="index" :class="`grid-item-${index}`">
    <div :class="`img-${index}`">圖像</div>
    <div :class="`text-${index}`">衣服</div>
    <div :class="`price-${index}`">500元</div>
  </div>
</div>
</template>

<style lang="postcss" scoped>
@import "../styles/base/_variables.css";
@import "../styles/base/_global.css";
@import "../styles/modules/_shoplist.css";
</style>

