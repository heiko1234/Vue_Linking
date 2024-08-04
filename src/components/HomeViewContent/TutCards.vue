<template>
  <div class="card">
    <div class="card-tag">{{ tag }}</div>
    <!-- <img :src="imageUrl" alt="Card Image" class="card-image" /> -->
    <img src="@/assets/datascience.jpeg" alt="Card Image" class="card-image" />
    <h2>{{ title }}</h2>
    <div class="card-description">
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TutCard',
  props: {
    imageUrl: {
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
  align-items: center;
  padding: 16px;
  margin: 5px 20px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card-tag {
  padding: 4px 8px;
  background-color: #007bff;
  color: #fff;
  border-radius: 4px;
  align-self: flex-start;
}

.card-image {
  width: 100%;
  max-width: 200px;
  min-width: 200px;
  max-height: 200px;
  object-fit: cover;
  border-radius: 4px;
}

.card-description {
  margin-top: 16px;
  text-align: center;
}
</style>
