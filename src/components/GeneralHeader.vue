<!-- Header: 45min -->

<template>
  <div class="header">
    <a href="">
      <img src="../assets/Apollon.jpeg" alt="Logos" class="logo" />
    </a>
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
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

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

.logo:hover {
  cursor: pointer;
  transform: scale(1.07);
  box-shadow: 0 0 10px rgb(252, 250, 250);
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
