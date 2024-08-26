<template>
  <div class="bucket">
    <h2 class="bucket-title">{{ bucket_title }}</h2>
    <ul class="bucket-list">
      <li v-for="item in bucket_list" :key="item.id">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BucketComponent',
  props: {
    bucket_title: String,
    bucket_list: Array
  }
}
</script>

<style scoped>
.bucket {
  display: block;
  padding: 1rem;
  margin: 1rem;
  background-color: transparent;
  border: 2px solid var(--cyan-10);
  min-width: 250px;
  max-width: 250px;
  max-height: 350px;
  border-radius: 0.5rem;
}

.bucket-title {
  font-size: 2rem;
  font-family: Arial, Helvetica, sans-serif;
  color: var(--cyan-10);
  text-align: center;
  padding: 0;
  margin: 0.5rem;
}

.bucket-list {
  padding: 10px;
  margin: 10px;
  font-size: 1.1rem;
}
</style>
