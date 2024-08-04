<!-- About Content -->

<template>
  <div class="AboutContentContainer">
    <div class="about-text">
      <h1>About</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nisl a lacinia
        tincidunt, nunc nunc lacinia nunc, nec ultricies nunc nunc auctor nunc. Sed id semper nunc.
        Sed auctor, nunc a ultrices tincidunt, nunc nunc lacinia nunc, nec ultricies nunc nunc
        auctor nunc.
      </p>
    </div>
    <div class="about-graphic">
      <img src="@/assets/datascience.jpeg" alt="About Graphic" style="width: 50%; height: auto" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutContent'
}
</script>

<style>
.AboutContentContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f2f2f2;
}

.about-text {
  flex: 1;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.about-graphic {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 2rem;
}

.about-graphic img {
  max-width: 50%;
  max-height: 50%;
}
</style>
