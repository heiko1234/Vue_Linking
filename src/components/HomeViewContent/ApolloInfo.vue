<!-- General Apollo Info -->

<template>
  <div class="InfoContentContainer">
    <h1 class="info-title">{{ product_title }}</h1>
    <div class="InfoContentContainerContent">
      <div class="info-text">
        <div class="subtitle">
          {{ product_subtitle }}
        </div>
        <div class="shortdescription">
          {{ product_shortdescription }}
        </div>
        <p>
          {{ info_text }}
        </p>
        <div>
          <button class="button_video" @click="goToVideo">
            <img class="button_icon" src="" alt="" />
            Video
          </button>
          <button class="button_start" @click="$router.push('/services')">
            <img class="button_icon" src="" alt="" />
            Get Started
          </button>
        </div>
      </div>
      <div class="info-graphic">
        <img src="@/assets/datascience.jpeg" alt="About Graphic" style="width: 50%; height: auto" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ApolloInfo',
  props: {
    product_title: {
      type: String,
      required: true
    },
    product_subtitle: {
      type: String,
      required: true
    },
    product_shortdescription: {
      type: String,
      required: true
    },
    info_text: {
      type: String,
      required: true
    }
  },
  methods: {
    goToVideo() {
      window.open('https://www.youtube.com/watch?v=9bZkp7q19f0')
    }
  }
}
</script>

<style scoped>
.InfoContentContainer {
  display: block;
  font-family: Arial, Helvetica, sans-serif;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

.InfoContentContainerContent {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
}

.info-title {
  font-size: 4rem;
  color: black;
  text-align: center;
  margin-top: 5px;
  margin-bottom: 5px;
}

.subtitle {
  font-size: 2.5rem;
  font-family: 'Times New Roman', Times, serif;
  font-weight: bold;
  color: var(--cyan-10);
  text-align: center;
  margin-bottom: 1rem;
}

.shortdescription {
  font-size: 1.8rem;
  font-family: 'Times New Roman', Times, serif;
  font-weight: bold;
  color: black;
  text-align: center;
  margin-bottom: 1rem;
}

.info-text {
  flex: 1;
  padding: 1rem;
  padding-left: 4rem;
  font-size: 1rem;
  color: black;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.button_video {
  background-color: transparent;
  color: var(--cyan-10);
  align-items: center;
  font-size: 1.2rem;
  font-weight: bold;
  border: 2px solid var(--cyan-10);
  border-radius: 20px;
  padding: 10px 10px;
  margin: 10px;
  cursor: pointer;
}

.button_icon {
  width: 20px;
  height: 20px;
  margin-right: 10px;
}

.button_video:hover {
  background-color: var(--cyan-9);
  color: white;
  font-size: 20px;
  font-weight: bold;
  box-shadow: 0 0 15px var(--cyan-9);
}

.button_start {
  background-color: var(--cyan-10);
  color: white;
  font-size: 1.2rem;
  font-weight: bold;
  border: 2px solid var(--cyan-10);
  border-radius: 20px;
  padding: 10px 10px;
  margin: 10px;
  cursor: pointer;
}

.button_start:hover {
  background-color: green;
  color: white;
  font-size: 22px;
  font-weight: bold;
  border: 2px solid green;
  box-shadow: 0 0 15px green;
}

.info-graphic {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
  padding-bottom: 20px;
  max-height: 50%;
  max-width: 50%;
}

.info-graphic img {
  width: 70%;
  height: auto;
  transform: scale(1.5);
  border-radius: 20px;
  box-shadow: 0 0 15px var(--cyan-10);
}
</style>
