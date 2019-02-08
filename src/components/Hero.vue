<template>
  <div class="container hero">
    <div class="hero-contents">
      <h1 class="hero-title">Welcome to the Pickleheads Club</h1>
      <p>
        <i class="hero-subtitle">We build really stupid shit.</i>
      </p>
      <a class="button hero-button"
         data-scroll
         href="#projects">
        See Projects
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
};
</script>

<style scoped>
.hero {
  background: url('/img/background.jpg') no-repeat center bottom;
  background-size: cover;
  height: 100vh;
}

.hero-title {
  text-align: center;
}

.hero-subtitle {
  text-align: center;
  color: var(--grey);
  font-family: 'Playfair Display', sans-serif;
  font-size: 1.4rem;
}

@media (max-width: 576px) {
  .hero-subtitle {
    font-size: 1.2rem;
  }
}

.hero-contents {
  margin-top: 25vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero-button {
  margin-top: 20px;
  background-color: var(--mint);
  color: white;
}
</style>
