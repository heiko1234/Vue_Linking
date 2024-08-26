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
  font-family: Arial, Helvetica, sans-serif;
  color: var(--cyan-10);
  text-align: center;
  padding: 0;
  margin: 0.5rem;
}

.RoadmapContainerContent {
  display: flex;
  align-items: top;
  width: auto;
  overflow-x: auto;
  padding: 2rem;
  margin: 50px;
}
</style>
