<!-- Header: 45min -->

<template>
  <div class="header">
    <h1 class="title">{{ promotion_text }}</h1>
    <!-- <h2 class="subtitle">Subtitle</h2> -->
  </div>
</template>

<script>
export default {
  name: 'PromotionHeader',
  props: ['promotion_text']
}
</script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.header {
  background-color: blue;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px;
  width: 100%;
}

.title {
  text-align: center;
  font-size: 20px;
  font-weight: bold;
  color: white;
}
</style>
