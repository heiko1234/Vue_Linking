<template>
  <div class="FAQContainer">
    <h1 class="title">{{ title }}</h1>
    <div class="ContainerContent">
      <div class="accordion">
        <div v-for="(item, index) in faq" :key="index" class="accordion-item">
          <div class="accordion-header" @click="toggleAccordion(index)">
            <div class="accodrion-header-items">
              {{ item.Question }}
              <img
                src="@/assets/arrow_down.png"
                alt="Arrow Down"
                :class="{ 'arrow-down': true, open: item.open }"
              />
              <!-- <img :src="item.arrow" alt="Arrow Down" class="arrow-down" /> -->
            </div>
          </div>
          <div v-if="item.open" class="accordion-content">
            {{ item.Answer }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FAQ',
  props: ['faq'],
  data() {
    return {
      title: 'Frequently Asked Questions'
    }
  },
  methods: {
    toggleAccordion(index) {
      this.faq[index].open = !this.faq[index].open
    }
  }
}
</script>

<style scoped>
.FAQContainer {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: #f5f4f4;
}

.ContainerContent {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
}

.title {
  font-size: 2rem;
  color: var(--cyan-10);
  text-align: center;
}

.accordion {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
}
.accordion-item {
  margin-bottom: 1rem;
  border: 1px solid #ddd;
  border-radius: 0.5rem;
}

.accordion-header {
  padding: 1rem;
  background-color: #f5f5f5;
  cursor: pointer;
}

.accodrion-header-items {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.arrow-down {
  width: 20px;
  height: 20px;
  transform: rotate(0deg);
  transition: transform 0.3s;
}

.arrow-down.open {
  width: 20px;
  height: 20px;
  transform: rotate(90deg);
  transition: transform 0.3s;
}

.accordion-content {
  padding: 1rem;
  background-color: #fff;
}
</style>
