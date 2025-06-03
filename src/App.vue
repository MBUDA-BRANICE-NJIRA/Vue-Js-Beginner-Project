<!-- Templete Section -->
<template>
  <div class="app-container">
    <NavBar />
    <header class="header">
      <h1>{{ heading }}</h1>
      <p>{{ description }}</p>
      <button class="cta-button" @click="sayhello">{{ buttonText }}</button>
    </header>
    <About />
    <Testimonial />
    <ContactUs />
    <FooTer />
  </div>
</template>
<!-- Scripting Section -->
<script>
import NavBar from './components/NavBar.vue';
import FooTer from './components/FooTer.vue';
import About from './components/About.vue';
import Testimonial from './components/Testimonial.vue';
import ContactUs from './components/ContactUs.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    About,
    Testimonial,
    ContactUs,
    FooTer
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
  }
};
</script>
<!-- styling section -->
<style scoped>
.app-container {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f1f5f9; /* light slate */
  min-height: 100vh;
}

.header {
  background-color: #e2e8f0; /* slate-200 */
  padding: 3rem 1.5rem;
  text-align: center;
  border-radius: 0.5rem;
  margin: 2rem auto;
  max-width: 600px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h1 {
  color: #0f172a; /* slate-900 */
  font-size: 2rem;
  margin-bottom: 1rem;
}

p {
  color: #475569; /* slate-600 */
  font-size: 1rem;
  margin-bottom: 1.5rem;
}

.cta-button {
  background-color: #3b82f6; /* blue-500 */
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  border-radius: 0.375rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #2563eb; /* blue-600 */
}
</style>
