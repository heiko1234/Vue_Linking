<template>
  <div class="card">
    <div class="card-tag">{{ tag }}</div>

    <img src="@/assets/datascience.jpeg" alt="Mate" class="card-image" />

    <h2>{{ name }}</h2>
    <div class="card-description">
      <p>{{ description }}</p>
    </div>
    <div class="card-controls">
      <button class="card-control-button">Info</button>
      <button class="card-control-button">Go To</button>
    </div>
  </div>
</template>

<!-- Find a solution for the not showing image -->
<!-- https://www.lichter.io/articles/nuxt3-vue3-dynamic-images/ -->
<!-- https://stackoverflow.com/questions/69696677/vite-vue-3-require-is-not-defined-when-using-image-source-as-props -->
<!-- https://vitejs.dev/guide/features.html#static-assets -->

<script>
export default {
  name: 'MateCard',
  data() {
    return {
      name: 'Mate',
      description:
        'Data Science is the future of technology. Learn how to use data to make informed decisions.',
      tag: 'Modelling'
    }
  }
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  width: 300px;
  min-width: 300px;
  height: 350px;
  align-items: center;
  margin: 5px 20px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  position: relative;
  overflow: hidden;
}

.card-tag {
  padding: 4px 8px;
  background-color: #1900ff;
  color: #fff;
  border-radius: 4px;
  align-self: flex-start;
  margin: 8px;
  position: absolute;
  top: 8px;
  left: 8px;
  z-index: 1;
}

.card-image {
  width: 100%;
  height: 100px;
  object-fit: cover;
  border-radius: 4px;
}

.card-description {
  margin-top: 8px;
  padding: 0 16px;
  text-align: center;
  height: 140px;
}

.card-controls {
  display: flex;
  margin-left: auto;
  justify-content: space-between;
  align-items: center;
  margin-top: 16px;
  padding: 0 16px;
  margin: 16px 0;
}

.card-control-button {
  margin-right: 8px;
  padding: 8px 20px;
  background-color: #1900ff;
  color: #fff;
  border: none;
  border-radius: 16px;
  cursor: pointer;
}

.card-control-button:hover {
  background-color: #0d00b3;
}
</style>
