<!-- General Apollo Info -->

<template>
  <div class="AboutContentContainer">
    <h1 class="about-title">About</h1>
    <div class="AboutContentContainerContent">
      <div class="about-text">
        <p>
          {{ about_text }}
        </p>
      </div>

      <div class="rightcontent">
        <div class="button-container">
          <button class="button" @click="changeGraphic('graphic1')">App 1</button>
          <button class="button" @click="changeGraphic('graphic2')">App 2</button>
          <button class="button" @click="changeGraphic('graphic3')">App 3</button>
        </div>
        <div class="graphic-container">
          <img :src="selectedGraphic" alt="Graphic" class="graphic" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Apollon2 from '@/assets/Apollon2.jpeg'
import Apollon3 from '@/assets/Apollon3.jpeg'
import Apollon4 from '@/assets/Apollon4.jpeg'

export default {
  name: 'AboutInfo',
  props: {
    about_text: {
      type: String,
      required: true
    }
  },

  data() {
    return {
      selectedGraphic: ''
    }
  },
  methods: {
    changeGraphic(graphic) {
      if (graphic === 'graphic1') {
        this.selectedGraphic = Apollon2
      } else if (graphic === 'graphic2') {
        this.selectedGraphic = Apollon3
      } else if (graphic === 'graphic3') {
        this.selectedGraphic = Apollon4
      }
    }
  },
  mounted() {
    this.selectedGraphic = Apollon2
  }
}
</script>

<style>
.AboutContentContainer {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: #f5f4f4;
}

.AboutContentContainerContent {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
}

.about-title {
  font-size: 2rem;
  color: rgb(0, 161, 148);
  text-align: center;
}

.about-text {
  flex: 1;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  display: flex;
}

.rightcontent {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
}

.button {
  margin: 0.5rem;
  padding: 0.5rem 1rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: transparent;
  color: #333;
  cursor: pointer;
}

.button.selected {
  background-color: blue;
  color: white;
}

.button:not(.selected):hover {
  border-color: blue;
}

.graphic-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.graphic {
  max-width: 100%;
  height: auto;
}
</style>
