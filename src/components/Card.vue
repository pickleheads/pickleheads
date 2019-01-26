<template>
  <div class="card">
    <div
      class="card-image"
      :style="{ backgroundImage: 'url(' + project.image + ')' }"
    ></div>
    <div class="card-info-container">
      <h3 class="car-title">{{ project.title }}</h3>
      <p class="card-description">{{ project.description }}</p>
    </div>
    <div class="card-actions-container">
      <a
        v-for="action in project.actions"
        class="button card-button"
        :key="action.name"
        :href="action.url"
      >
        {{ action.name }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    project: {},
  },
};
</script>

<style scoped>
.card {
  box-shadow: 0 27px 55px 0 rgba(0, 0, 0, 0.3),
    0 17px 17px 0 rgba(0, 0, 0, 0.15);
  height: 300px;
  min-height: 300px;
  min-width: 300px;
  display: flex;
  flex-direction: column;
}

.card-image {
  width: 100%;
  background: no-repeat center center;
  background-size: cover;
  flex: 1 1 140px;
}

.card-info-container {
  border-bottom: 1px solid var(--grey);
  padding: 10px 10px;
  flex: 1 1 auto;
}

.card-description {
  font-size: 0.88rem;
  color: var(--grey);
}

.card-actions-container {
  padding: 6px 10px;
  flex: 0 0 auto;
  display: block;
}

.button.card-button {
  width: 80px;
  background-color: transparent;
  box-shadow: none;
  font-weight: bold;
}

.button.card-button:hover {
  transition: all 150ms linear;
  background-color: #e5e5e5;
}
</style>
