<template>
  <div class="card">
    <div class="card-tag">{{ tag }}</div>
    <!-- <img :src="imageUrl" alt="Card Image" class="card-image" /> -->
    <!-- <img src="@/assets/datascience.jpeg" alt="Card Image" class="card-image" /> -->
    <!-- <img :src="require('@/assets/' + imageName)" alt="Card Image" class="card-image" /> -->
    <!-- <img :src="imageUrl(imageName)" alt="Card Image" class="card-image" /> -->
    <!-- <img :src="imagePath" :alt="imageName" class="card-image" /> -->
    <img src="@/assets/datascience.jpeg" :alt="imageName" class="card-image" />
    <!-- <img :src="`../assets/${imageName}.jpeg`" alt="Card Image" class="card-image" /> -->

    <h2>{{ title }}</h2>
    <div class="card-description">
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<!-- Find a solution for the not showing image -->
<!-- https://www.lichter.io/articles/nuxt3-vue3-dynamic-images/ -->
<!-- https://stackoverflow.com/questions/69696677/vite-vue-3-require-is-not-defined-when-using-image-source-as-props -->
<!-- https://vitejs.dev/guide/features.html#static-assets -->

<script>
export default {
  name: 'TutCard',
  props: {
    src: {
      type: String
    },
    title: {
      type: String
    },
    description: {
      type: String
    },
    tag: {
      type: String
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
  cursor: pointer;
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
  height: auto;
  object-fit: cover;
  border-radius: 4px;
}

.card-description {
  margin-top: 16px;
  text-align: center;
}
</style>
