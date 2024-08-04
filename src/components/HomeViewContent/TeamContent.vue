<template>
  <div class="TeamContainer">
    <h1 class="title">{{ title }}</h1>
    <h2 class="subtitle">{{ subtitle }}</h2>
    <div class="TeamContainerContent">
      <div class="team-member">
        <img src="@/assets/Team_pics/femal_pic.jpeg" alt="Developer 1" class="team-member-image" />
      </div>
      <div class="team-member">
        <img src="@/assets/Team_pics/male_pic.jpeg" alt="Developer 1" class="team-member-image" />
      </div>
      <div class="team-member">
        <img src="@/assets/Team_pics/male_pic2.jpeg" alt="Developer 1" class="team-member-image" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamInfo',
  data() {
    return {
      title: 'Team',
      subtitle: 'Apollon is created by a team of developers who are passionate about Data Science.'
    }
  }
}
</script>

<style scoped>
.TeamContainer {
  display: block;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  background-color: #f5f4f4;
}

.TeamContainerContent {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
}

.title {
  font-size: 2rem;
  color: rgb(0, 161, 148);
  text-align: center;
}

.subtitle {
  font-size: 1.2rem;
  color: black;
  text-align: center;
}

.team-member {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  padding: 1rem;
}

.team-member-image {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
