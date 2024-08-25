<template>
  <!-- make a for loop for all tutorial in tutorials -->
  <div class="tutorials-container">
    <h1 class="tutorial-title">Tutorials</h1>

    <div class="tutorial-controls">
      <!-- Tutorial control goes here-->
      <button class="tutorial-control-button">
        <img
          class="tutorial-control-button-icon"
          src="@/assets/arrow_left.png"
          alt="Tutorial Image"
          @click="handleTutorialClickleft"
        />
      </button>
      <button class="tutorial-control-button">
        <img
          class="tutorial-control-button-icon"
          src="@/assets/arrow_right.png"
          alt="Tutorial Image"
          @click="handleTutorialClickright"
        />
      </button>
    </div>

    <div class="tutorial-content">
      <!-- Tutorial content goes here -->
      <TutCard
        v-for="tutorial in tutorials"
        :key="tutorial.title"
        :tutorial="tutorial"
        :title="tutorial.title"
        :tag="tutorial.tag"
        :description="tutorial.description"
        :src="tutorial.image"
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
  props: ['tutorials'],
  methods: {
    handleTutorialClickleft() {
      console.log('Left button clicked')
      const tutorialContent = document.querySelector('.tutorial-content')
      tutorialContent.scrollLeft -= 200 // Adjust the scroll distance as needed
    },
    handleTutorialClickright() {
      console.log('Right button clicked')
      const tutorialContent = document.querySelector('.tutorial-content')
      tutorialContent.scrollLeft += 200 // Adjust the scroll distance as needed
    }
  }
}
</script>

<style scoped>
.tutorials-container {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: transparent;
}

.tutorial-title {
  font-size: 2rem;
  color: var(--cyan-10);
  text-align: center;
  padding: 0;
  margin: 0.5rem;
}

.tutorial-content {
  display: flex;
  width: auto;
  flex-wrap: nowrap;
  overflow-y: auto;
  overflow-x: hidden;
  margin: 20px 30px;
}

.tutorial-controls {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
}

.tutorial-control-button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: var(--cyan-10);
  margin: 0 1rem;
  padding: 0.5rem;
}

.tutorial-control-button-icon {
  height: 2rem;
  width: 2rem;
}
</style>
