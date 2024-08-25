<template>
  <div class="TeamContainer">
    <h1 class="title">{{ title }}</h1>
    <h2 class="subtitle">{{ subtitle }}</h2>
    <div class="TeamContainerContent">
      <div class="team-member">
        <img src="@/assets/Team_pics/femal_pic.jpeg" alt="Developer 1" class="team-member-image" />
        <h3>Silke Kulinna</h3>
      </div>
      <div class="team-member">
        <img src="@/assets/Team_pics/male_pic.jpeg" alt="Developer 1" class="team-member-image" />
        <h3>Tobias Kulinna</h3>
      </div>
      <div class="team-member">
        <img src="@/assets/Team_pics/male_pic.jpeg" alt="Developer 1" class="team-member-image" />
        <h3>Heiko Kulinna</h3>
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
      subtitle: 'Apollo is created by a team of developers who are passionate about Data Science.'
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
  font-size: 3rem;
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(0, 161, 148);
  text-align: center;
  padding: 0;
  margin: 0.5rem;
}

.subtitle {
  font-size: 1.2rem;
  color: black;
  text-align: center;
}

.team-member {
  position: relative;
  margin: 10px;
}

.team-member h3 {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.2rem;
  color: black;
  text-align: center;
  opacity: 0;
}

.team-member:hover h3 {
  opacity: 1;
  transition: opacity 0.5s ease-in-out;
  color: black;
}

.team-member:hover img {
  filter: grayscale(100%);
  opacity: 0.4;
}

.team-member-image {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
