<template>
  <div>
    <!-- <GeneralHeader /> -->
    <!-- <SubHeader /> -->
    <!-- Other content for HomeView can go here -->
    <PromotionHeader :promotion_text="promotion_text" />
    <HomeViewHeaderVue @scroll-to-section="handleScrollToSection" />
    <div class="scroll_div">
      <section id="Apollo">
        <ApolloInfo :info_text="info_text" />
      </section>

      <section id="About">
        <AboutContent :about_text="about_text" />
      </section>

      <section id="Tutorials">
        <TutorialsContent :tutorials="tutorials" />
      </section>

      <section id="Team">
        <TeamInfo />
      </section>

      <section id="RoadmapContent">
        <RoadmapContent :roadmap="roadmap" />
      </section>

      <section id="FAQ">
        <FAQ :faq="faq" />
      </section>
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
import RoadmapContent from '@/components/HomeViewContent/Roadmap.vue'
import FAQ from '@/components/HomeViewContent/FAQ.vue'

export default {
  name: 'HomeView',
  components: {
    PromotionHeader,
    HomeViewHeaderVue,
    ApolloInfo,
    AboutContent,
    TutorialsContent,
    TeamInfo,
    RoadmapContent,
    FAQ
  },
  data() {
    return {
      promotion_text: 'I can write anything here, that i like to promote',
      info_text:
        'This is about the product, i like to promote here. Give general Informaiton about the product here.',
      about_text:
        'Lorem ipsum dolor sit amet, consectatur. Anything about the product itself and its modules. What is possible, what is not possible ',
      tutorials: [
        {
          title: 'Tutorial 1',
          tag: 'Beginner',
          description: 'This is a tutorial for beginners',
          image: 'datascience'
        },
        {
          title: 'Tutorial 2',
          tag: 'Intermediate',
          description: 'This is a tutorial for intermediate users',
          image: 'Apollon4'
        },
        {
          title: 'Tutorial 3',
          tag: 'Advanced',
          description: 'This is a tutorial for advanced users',
          image: 'datascience'
        },
        {
          title: 'Tutorial 4',
          tag: 'Advanced',
          description: 'This is a master tutorial for advanced users',
          image: 'datascience'
        },
        {
          title: 'Tutorial 5',
          tag: 'Advanced',
          description: 'This is a master tutorial for advanced users',
          image: 'datascience'
        },
        {
          title: 'Tutorial 6',
          tag: 'Advanced',
          description: 'This is a master tutorial for advanced users',
          image: 'datascience'
        }
      ],
      roadmap: [
        {
          title: 'Now',
          list: ['Landing Page', 'Onboarding']
        },
        {
          title: 'Next',
          list: ['Data Science Tutorials', 'Data Science Projects', 'Data Science Blog']
        },
        {
          title: 'Later',
          list: ['Data Science Community', 'Data Science Marketplace']
        }
      ],
      faq: [
        {
          Question: 'What is Apollo?',
          Answer: 'Apollo is a greek god who brought the humans the light'
        },
        { Question: 'How to start?', Answer: "Start by clicking on the 'Get Started' button" },
        {
          Question: 'What is the purpose of Apollon?',
          Answer:
            'Apollon is a platform for Data Science enthusiasts to learn, share and grow, it is to create and manage all aspects of models, so that the whole data science worklfow and model implementations is covered very effectively.'
        }
      ]
    }
  },
  methods: {
    handleScrollToSection(section) {
      const element = document.getElementById(section)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
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
