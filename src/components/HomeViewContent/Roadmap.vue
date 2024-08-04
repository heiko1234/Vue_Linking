<template>
  <div class="RoadmapContainer">
    <h1 class="title">{{ title }}</h1>
    <div class="RoadmapContainerContent">
      <div class="bucket">
        <h2 class="bucket-title">Now</h2>
        <ul class="bucket-list">
          <li v-for="item in now" :key="item">{{ item }}</li>
        </ul>
      </div>

      <div class="bucket">
        <h2 class="bucket-title">Next</h2>
        <ul class="bucket-list">
          <li v-for="item in next" :key="item">{{ item }}</li>
        </ul>
      </div>

      <div class="bucket">
        <h2 class="bucket-title">Future</h2>
        <ul class="bucket-list">
          <li v-for="item in future" :key="item">{{ item }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Roadmap',
  data() {
    return {
      title: 'Roadmap',
      now: ['Landing Page', 'Onboarding Process simplification'],
      next: ['Data Science Tutorials', 'Data Science Projects', 'Data Science Blog'],
      future: ['Data Science Community', 'Data Science Marketplace', 'Data Science Platform']
    }
  }
}
</script>

<style scoped>
.RoadmapContainer {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: transparent;
}

.title {
  font-size: 2rem;
  color: rgb(6, 43, 255);
  text-align: center;
}

.RoadmapContainerContent {
  display: flex;
  justify-content: center;
  align-items: top;
  flex-wrap: nowrap;
  overflow-x: auto;
  padding: 1rem;
  margin: 1rem;
}

.bucket {
  display: block;
  padding: 1rem;
  margin: 1rem;
  background-color: transparent;
  border: 1px solid blue;
  min-width: 250px;
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
