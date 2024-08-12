<template>
  <div class="RoadmapContainer">
    <h1 class="title">{{ title }}</h1>
    <div class="RoadmapContainerContent">
      <bucket-component
        v-for="bucket in roadmap"
        :key="bucket.title"
        :bucket_title="bucket.title"
        :bucket_list="bucket.list"
      />
    </div>
  </div>
</template>

<script>
import BucketComponent from '@/components/HomeViewContent/RoadmapContainer.vue'

export default {
  name: 'RoadmapContent',
  components: {
    BucketComponent
  },
  props: ['roadmap'],
  data() {
    return {
      title: 'Roadmap'
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
  align-items: top;
  width: auto;
  overflow-x: auto;
  padding: 2rem;
  margin: 50px;
}

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
