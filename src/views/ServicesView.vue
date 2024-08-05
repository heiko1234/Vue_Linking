<!-- Header: 45min -->

<template>
  <div class="header">
    <div class="leftside">
      <img class="header_logo" src="@/assets/Apollon.jpeg" alt="Apollon" />
    </div>
    <div class="center">
      <h1 class="title">Apollo Services</h1>
    </div>
    <div class="rightside"></div>
  </div>

  <div class="scroll_div">
    <section class="scroll_div_section" id="Modelling">
      <MateCard />
      <NavigatorCard />
    </section>
  </div>
</template>

<!-- script -->
<script>
import MateCard from '@/components/ServiceContent/MateCard.vue'
import NavigatorCard from '@/components/ServiceContent/NavigatorCard.vue'

export default {
  name: 'ServicesView',
  components: {
    MateCard,
    NavigatorCard
  }
}
</script>

<!-- styles -->
<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.leftside {
  width: 25%;
}

.center {
  width: 500%;
}

.rightside {
  width: 25%;
}

.header {
  background-color: blue;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px;
  width: 100%;
}

.header_logo {
  width: 75px;
  height: 75px;
  margin-right: auto;
}

.title {
  text-align: center;
  font-size: 20px;
  font-weight: bold;
  color: white;
}

.scroll_div {
  padding: 10px;
  box-sizing: border-box;
  width: 90%;
  height: 90%;
}

.scroll_div_section {
  display: flex;
  flex-wrap: wrap;
  overflow-x: auto;
  flex: 0 0 50%;
  padding: 10px;
  box-sizing: border-box;
}
</style>
