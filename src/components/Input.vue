<template>
  <div class="custom-label" @click="redirectTo">
    <span>{{ text }}</span>
    <i class="bi bi-send"></i>
  </div>
</template>

<script>
import 'bootstrap-icons/font/bootstrap-icons.css';

export default {
  props: {
    text: {
      type: String,
      required: true
    },
    url: {
      type: String,
      required: true
    }
  },
  methods: {
    redirectTo() {
      window.open(this.url, '_blank');
    }
  }
};
</script>

<style scoped>
.custom-label {
  width: 100%;
  background-color: transparent;
  border: 2px solid white;
  border-radius: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
  padding: 0.4rem 1rem;
  font-size: 2rem;
  font-weight: bold;
  cursor: pointer;
}

.custom-label span {
  flex: 1;
  text-align: center;
}

.custom-label i {
  font-size: 1.7rem;
}

@media (max-width: 950px) {
  .custom-label {
    padding: 1rem 1rem;
  }
}

@media (max-width: 500px) {
.custom-label {
  font-size: 1.1rem;
  padding: 0.2rem 1rem;
}
}
</style>
