<!-- Header: 45min -->

<template>
  <div class="header">
    <h2 class="title">Sub Header</h2>
    <!-- <h2 class="subtitle">Subtitle</h2> -->
  </div>
</template>

<script>
export default {
  name: 'SubHeader'
}
</script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.header {
  background-color: rgb(225, 0, 255);
  display: flex;
  align-items: center;
  padding: 10px;
  width: 100%;
}

.title {
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  color: white;
}

.subtitle {
  text-align: center;
  font-size: 16px;
  color: gray;
}
</style>
