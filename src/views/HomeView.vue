<template>
  <div>
    <!-- <GeneralHeader /> -->
    <!-- <SubHeader /> -->
    <!-- Other content for HomeView can go here -->
    <PromotionHeader :promotion_text="promotion_text" />
    <HomeViewHeaderVue />
  </div>
</template>

<script>
// import HomeViewHeaderVue from '@/components/HomeViewHeader.vue'
// import GeneralHeader from '../components/GeneralHeader.vue'
// import SubHeader from '../components/SecondHeader.vue'
import PromotionHeader from '../components/PromotionHeader.vue'
import HomeViewHeaderVue from '../components/HomeViewHeader.vue'

export default {
  name: 'HomeView',
  components: {
    // GeneralHeader,
    // SubHeader,
    PromotionHeader,
    HomeViewHeaderVue
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
</style>
