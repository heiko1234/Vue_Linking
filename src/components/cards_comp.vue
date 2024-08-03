<template>
  <div class="card">
    <h4>Card Main Body</h4>
    <div class="card-header">
      <h3>Card Titles</h3>
    </div>

    <div class="card-body">
      <p>Card Body</p>
    </div>

    <div class="card-footer"></div>
  </div>
</template>

<script setup></script>

<style scoped>
.card {
  border: 4px solid #20c211;
  border-radius: 10px;
  margin: 10px;
  padding: 10px;
  width: 300px;
}

.card-header {
  background-color: #aa1515;
  border-bottom: 1px solid #e41010;
  border-radius: 4px 4px 0 0;
  padding: 10px;
}

.card-body {
  padding: 10px;
}

.card-footer {
  background-color: #200808;
  border-top: 1px solid #571313;
  border-radius: 0 0 4px 4px;
  padding: 10px;
}
</style>
