<template>
  <div class="header">
    <img src="../assets/Apollon.jpeg" alt="Logos" class="logo" />
    <h1 class="title">Header</h1>
    <!-- <h2 class="subtitle">Subtitle</h2> -->
  </div>
</template>

<script>
export default {
  name: 'GeneralHeader'
}
</script>

<style scoped>
.header {
  background-color: blue;
  display: flex;
  align-items: center;
  padding: 10px;
  width: 100%;
}

.logo {
  width: 50px;
  height: 50px;
  margin-right: 10px;
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
