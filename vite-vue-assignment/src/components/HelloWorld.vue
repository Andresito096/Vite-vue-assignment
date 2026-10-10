<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
  </div>
</template>

<style scoped>
h1 {
  color: #175ca8;
  font-weight: 1000;
  font-size: 2.6rem;
  position: relative;
  top: -30px;
}

h2 {
  color: #444;
}

h3 {
  font-size: 1.2rem;
}
</style>
