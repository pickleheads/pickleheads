<template>
  <div id="app" class="main">
    <Hero />
    <Projects />
    <Footer />
  </div>
</template>

<script>
import Footer from './components/Footer.vue';
import Hero from './components/Hero.vue';
import Projects from './components/Projects.vue';

export default {
  name: 'app',
  components: {
    Footer,
    Hero,
    Projects,
  },
};
</script>

<style>
* {
  margin: 0;
  font-family: 'Roboto', sans-serif;
}

:root {
  --black: #292a2c;
  --grey: #999999;
  --mint: #3dd28d;
}

.main {
  width: 100vw;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Playfair Display', sans-serif;
  color: var(--black);
}

h1 {
  font-size: 3rem;
}

@media (max-width: 576px) {
  h1 {
    font-size: 2rem;
  }
}

.container {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.button {
  display: flex;
  overflow: hidden;
  background-color: #ccc;

  padding: 12px 12px;

  cursor: pointer;
  transition: all 150ms linear;
  text-align: center;
  white-space: nowrap;
  text-decoration: none;

  color: var(--black);
  border: 0 none;
  border-radius: 4px;

  font-size: 0.88rem;
  line-height: 1.3;

  justify-content: center;
  align-items: center;
  width: 160px;

  box-shadow: 2px 5px 10px #e5e5e5;
}

.button:hover {
  transition: all 150ms linear;
  opacity: 0.85;
}

.button:active {
  transition: all 150ms linear;
  opacity: 0.75;
}

.button:focus {
  outline: 1px dotted #959595;
  outline-offset: -4px;
}
</style>
