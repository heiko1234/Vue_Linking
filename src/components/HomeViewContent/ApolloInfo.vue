<!-- General Apollo Info -->

<template>
  <div class="InfoContentContainer">
    <h1 class="info-title">Apollo</h1>
    <div class="InfoContentContainerContent">
      <div class="info-text">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nisl a lacinia
          tincidunt, nunc nunc lacinia nunc, nec ultricies nunc nunc auctor nunc. Sed id semper
          nunc. Sed auctor, nunc a ultrices tincidunt, nunc nunc lacinia nunc, nec ultricies nunc
          nunc auctor nunc.
        </p>
      </div>
      <div class="info-graphic">
        <img src="@/assets/datascience.jpeg" alt="About Graphic" style="width: 50%; height: auto" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ApolloInfo'
}
</script>

<style>
.InfoContentContainer {
  display: block;
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
  font-size: 2rem;
  color: rgb(6, 43, 255);
  text-align: center;
}

.info-text {
  flex: 1;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.info-graphic {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
}

.info-graphic img {
  max-width: 50%;
  max-height: 50%;
}
</style>
