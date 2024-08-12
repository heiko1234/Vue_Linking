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

<style scopd>
.bucket {
  display: block;
  padding: 1rem;
  margin: 1rem;
  background-color: transparent;
  border: 1px solid blue;
  min-width: 250px;
  max-width: 250px;
  max-height: 350px;
  border-radius: 0.5rem;
}

.bucket-title {
  font-size: 1.5rem;
  color: blue;
  text-align: center;
}

.bucket-list {
  padding: 10px;
  margin: 10px;
}
</style>
