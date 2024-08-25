<!-- General Apollo Info -->

<template>
  <div class="AboutContentContainer">
    <h1 class="about-title">About</h1>
    <div class="AboutContentContainerContent">
      <div class="about-text">
        <p>
          {{ about_text }}
        </p>
        <p>
          {{ about_text2 }}
        </p>
        <p>
          {{ about_text3 }}
        </p>
      </div>

      <div class="rightcontent">
        <div class="button-container">
          <button
            class="button_about"
            :class="{ active: selectedButton === 'App 1' }"
            @click="changeGraphic('graphic1')"
          >
            Process Design
          </button>
          <button
            class="button_about"
            :class="{ active: selectedButton === 'App 2' }"
            @click="changeGraphic('graphic2')"
          >
            Modelling
          </button>
          <button
            class="button_about"
            :class="{ active: selectedButton === 'App 3' }"
            @click="changeGraphic('graphic3')"
          >
            Prediction Usage
          </button>
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
    },
    about_text2: {
      type: String,
      required: true
    },
    about_text3: {
      type: String,
      required: true
    }
  },

  data() {
    return {
      selectedGraphic: '',
      selectedButton: ''
    }
  },
  methods: {
    changeGraphic(graphic) {
      if (graphic === 'graphic1') {
        this.selectedGraphic = Apollon2
        this.setActiveButton('App 1')
      } else if (graphic === 'graphic2') {
        this.selectedGraphic = Apollon3
        this.setActiveButton('App 2')
      } else if (graphic === 'graphic3') {
        this.selectedGraphic = Apollon4
        this.setActiveButton('App 3')
      }
    },
    setActiveButton(button) {
      this.selectedButton = button
    }
  },
  mounted() {
    this.changeGraphic('graphic1')
  }
}
</script>

<style scoped>
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
  color: var(--cyan-10);
  text-align: center;
  margin: 0.5rem;
  padding: 0;
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

.button_about {
  background-color: transparent;
  color: var(--cyan-10);
  border: 1px solid var(--cyan-10);
  padding: 0.5rem 1rem;
  margin: 0 0.5rem;
  border-radius: 5px;
  cursor: pointer;
}

.button_about:hover:not(.active) {
  background-color: var(--cyan-8);
  color: white;
}

.button_about.active {
  background-color: var(--cyan-10);
  color: white;
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
