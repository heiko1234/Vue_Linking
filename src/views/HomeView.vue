<template>
  <div>
    <!-- <GeneralHeader /> -->
    <!-- <SubHeader /> -->
    <!-- Other content for HomeView can go here -->
    <PromotionHeader :promotion_text="promotion_text" />
    <HomeViewHeaderVue />
    <div class="scroll_div">
      <h1>any content</h1>
      <AboutContent />
    </div>
  </div>
</template>

<script>
// import HomeViewHeaderVue from '@/components/HomeViewHeader.vue'
// import GeneralHeader from '../components/GeneralHeader.vue'
// import SubHeader from '../components/SecondHeader.vue'
import PromotionHeader from '@/components/HomeViewContent/PromotionHeader.vue'
import HomeViewHeaderVue from '@/components/HomeViewContent/HomeViewHeader.vue'
import AboutContent from '@/components/HomeViewContent/AboutContent.vue'

export default {
  name: 'HomeView',
  components: {
    // GeneralHeader,
    // SubHeader,
    PromotionHeader,
    HomeViewHeaderVue,
    AboutContent
  },
  data() {
    return {
      promotion_text: 'I can write anything here, that i like to promote'
    }
  }
}
</script>

<style scoped>
/* Add any scoped styles for HomeView here */

.scroll_div {
  overflow-y: scroll;
}
</style>
