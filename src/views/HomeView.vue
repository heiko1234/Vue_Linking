<template>
  <div>
    <!-- <GeneralHeader /> -->
    <!-- <SubHeader /> -->
    <!-- Other content for HomeView can go here -->
    <PromotionHeader :promotion_text="promotion_text" />
    <HomeViewHeaderVue />
    <div class="scroll_div">
      <ApolloInfo />
      <AboutContent />
      <TutorialsContent />
      <TeamInfo />
      <Roadmap />
    </div>
  </div>
</template>

<script>
// import HomeViewHeaderVue from '@/components/HomeViewHeader.vue'
// import GeneralHeader from '../components/GeneralHeader.vue'
// import SubHeader from '../components/SecondHeader.vue'
import PromotionHeader from '@/components/HomeViewContent/PromotionHeader.vue'
import HomeViewHeaderVue from '@/components/HomeViewContent/HomeViewHeader.vue'
import ApolloInfo from '@/components/HomeViewContent/ApolloInfo.vue'
import AboutContent from '@/components/HomeViewContent/AboutContent.vue'
import TutorialsContent from '@/components/HomeViewContent/TutorialsContent.vue'
import TeamInfo from '@/components/HomeViewContent/TeamContent.vue'
import Roadmap from '@/components/HomeViewContent/Roadmap.vue'

export default {
  name: 'HomeView',
  components: {
    // GeneralHeader,
    // SubHeader,
    PromotionHeader,
    HomeViewHeaderVue,
    ApolloInfo,
    AboutContent,
    TutorialsContent,
    TeamInfo,
    Roadmap
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
  height: calc(100vh - 200px); /* Adjust the height as needed */
  overflow-y: auto;
}
</style>
