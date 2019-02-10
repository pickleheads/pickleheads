<template>
  <div class="testimonials-container">
    <h2 class="testimonial-header">Testimonials</h2>
    <Tweet v-for="id in tweetIds" :id="id" :key="id"></Tweet>
  </div>
</template>

<script>
import { Tweet } from 'vue-tweet-embed';

export default {
  name: 'Testimonials',
  components: { Tweet },
  data: function() {
    return {
      tweetIds: ['1079833398384910338', '9451789062'],
    };
  },
};
</script>

<style scoped>
  .testimonials-container {
    background-color: #eff0f2;
    padding: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .testimonial-header {
    margin-bottom: 20px;
  }
</style>
