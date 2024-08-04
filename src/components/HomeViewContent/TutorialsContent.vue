<template>
  <!-- make a for loop for all tutorial in tutorials -->
  <div class="tutorials-container">
    <h1 class="tutorial-title">Tutorials</h1>
    <div class="tutorial-content">
      <!-- Tutorial content goes here -->
      <TutCard
        v-for="tutorial in tutorials"
        :tutorial="tutorial"
        :title="tutorial.title"
        :tag="tutorial.tag"
        :description="tutorial.description"
        :image="tutorial.image"
      />
    </div>
  </div>
</template>

<script>
import TutCard from '@/components/HomeViewContent/TutCards.vue'

export default {
  name: 'TutorialsContent',
  components: {
    TutCard
  },
  data() {
    return {
      tutorials: [
        {
          title: 'Tutorial 1',
          tag: 'Beginner',
          description: 'This is a tutorial for beginners',
          image: '@/assets/datascience.jpeg'
        },
        {
          title: 'Tutorial 2',
          tag: 'Intermediate',
          description: 'This is a tutorial for intermediate users',
          image: '@/assets/datascience.jpeg'
        },
        {
          title: 'Tutorial 3',
          tag: 'Advanced',
          description: 'This is a tutorial for advanced users',
          image: '@/assets/datascience.jpeg'
        }
      ]
    }
  },
  mounted() {
    this.loadImages()
  },
  methods: {
    loadImages() {
      this.tutorials.forEach((tutorial) => {
        const img = new Image()
        img.src = tutorial.image
      })
    }
  }
}
</script>

<style>
.tutorials-container {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: transparent;
}

.tutorial-title {
  font-size: 2rem;
  color: rgb(6, 43, 255);
  text-align: center;
}

.tutorial-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
  margin: 1rem;
}
</style>
