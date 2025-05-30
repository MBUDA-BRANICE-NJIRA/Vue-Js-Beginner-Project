<!-- Templete Section -->
<template>
  <NavBar />
  <div class="header">
    <h1>{{ heading }}</h1>
    <p>{{ description }}</p>
    <button @click="sayhello">{{ buttonText }}</button>
  </div>
</template>

<!-- The script section -->
<script>
import NavBar from './components/NavBar.vue';

export default {
  name: 'App',
  components: {
    NavBar,
  },

  data() {
    return {
      heading: 'Welcome!',
      description: 'This is a simple Vue.js application.',
      buttonText: 'Read More'

    };
  },

  methods: {
    sayhello() {
      alert('Read More button clicked!');
    }
  },


 };
</script>


<!-- Stling Section -->
<style>
.header {
  background-color: lightgray;
  padding: 20px;
  text-align: center;
}
h1 {
  color: blue;
  text-align: center;
}
</style>
