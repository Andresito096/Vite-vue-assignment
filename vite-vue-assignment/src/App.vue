<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const message = ref('Click the button!')

function toggleMessage() {
  message.value = message.value === 'Click the button!' ? 'Button clicked!' : 'Click the button!'
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="My Very First Vue App Using Vite!" />
      <h2 class="author">By: Andres Orozco</h2>

      <p>
        Welcome to my very first Vue app using Vite! Using what I've learned so far in this class
        project, I can quickly build and test Vue components with modern tooling. I hope you find it
        informative and easy to navigate.
      </p>

      <h3>What I've Learned So Far</h3>

      <ul>
        <li>Understanding Vue's reactivity system</li>
        <li>Creating and using components</li>
        <li>Using Vite to create and manage Vue projects efficiently</li>
        <li>Adding HTML and CSS to enhance the app's structure and style</li>
        <li>Implementing interactivity with Vue's reactivity system</li>
      </ul>

      <p>{{ message }}</p>

      <button class="message-button" @click="toggleMessage">Click Me!</button>
    </div>
  </header>
</template>

<style scoped>
.container {
  max-width: 700px;
  margin: 50px auto;
  padding: 30px;
  background-color: #e8f4ff;
  border-radius: 12px;
  text-align: center;
  color: #222;
}

.author {
  font-style: italic;
  margin-top: -0.5rem;
  margin-bottom: 1rem;
}

h1 {
  color: #175ca8;
}

h2 {
  padding: -3rem;
  color: #444;
}

ul {
  display: inline-block;
  text-align: left;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
}

.message-button {
  background-color: #175ca8;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  cursor: pointer;
  border-radius: 600px;
  min-width: 120px;
  min-height: 45px;
}

.message-button:hover {
  background-color: #0d3c70;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-right: 0;
  }

  .logo {
    margin: 0 auto 1.5rem;
  }

  header .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    place-items: center;
    flex-wrap: wrap;
  }

  p {
    max-width: 600px;
    margin: 20px auto;
    line-height: 1.6;
    text-align: center;
  }
}
</style>
