<!-- Header: 45min -->

<template>
  <div class="header">
    <div class="header_items">
      <div class="left-section">
        <a href="">
          <img src="@/assets/Apollon.jpeg" alt="Logos" class="logo" />
        </a>

        <div class="middle_left">
          <button class="middle_left_button">About</button>
          <button class="middle_left_button">Tutorials</button>
          <button class="middle_left_button">Team</button>
          <button class="middle_left_button">Roadmap</button>
          <button class="middle_left_button">FAQ</button>
        </div>

        <!-- split left and right -->
      </div>
      <div class="right-section">
        <button class="button">Contact</button>
        <button class="button_start">Get Started</button>
      </div>
    </div>
    <div class="separator">
      <hr />
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeViewHeader'
}
</script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.header {
  background-color: rgb(255, 255, 255);
  display: block;
  align-items: center;
  justify-content: center;
  padding: 10px;
  width: 100%;
}

.header_items {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.left-section {
  display: flex;
  align-items: center;
  justify-content: left;
  margin: 3px;
  padding: 10px;
  width: 50%;
}

.middle_left {
  display: flex;
  align-items: left;
  justify-content: left;
  margin: 5px;
  padding: 10px;
  width: 50%;
}

.middle_left_button {
  background-color: transparent;
  color: grey;
  font-size: 16px;
  font-weight: bold;
  border: none;
  padding: 5px 10px;
  margin-right: 10px;
  cursor: pointer;
}
.middle_left_button:hover {
  text-decoration: underline;
}

.logo {
  width: 75px;
  height: 75px;
  margin-right: 10px;
}

.logo:hover {
  cursor: pointer;
  transform: scale(1.07);
  box-shadow: 0 0 10px rgb(252, 250, 250);
}

.right-section {
  display: flex;
  align-items: center;
  justify-content: right;
  margin: 30px;
  width: 50%;
}

.button {
  background-color: transparent;
  color: blue;
  font-size: 20px;
  font-weight: bold;
  border: 2px solid rgb(6, 43, 255);
  border-radius: 20px;
  padding: 10px 20px;
  margin: 0 5px;
  cursor: pointer;
}
.button:hover {
  background-color: blue;
  color: white;
  font-size: 20px;
  font-weight: bold;
  box-shadow: 0 0 15px rgba(0, 16, 247, 0.685);
}

.button_start {
  background-color: blue;
  color: white;
  font-size: 20px;
  font-weight: bold;
  border: 2px solid rgb(6, 43, 255);
  border-radius: 20px;
  padding: 10px 20px;
  margin: 0 5px;
  cursor: pointer;
}
.button_start:hover {
  background-color: green;
  color: white;
  font-size: 20px;
  font-weight: bold;
  border: 2px solid rgb(0, 128, 0);
  box-shadow: 0 0 15px rgba(0, 128, 0, 0.685);
}

.separator {
  width: 100%;
}
</style>
