<template>
  <div class="app-container">
    <NavBar />

    <header class="hero">
      <div class="hero-content">
        <h1>{{ heading }}</h1>
        <p>{{ description }}</p>
        <button class="cta-button" @click="sayhello">{{ buttonText }}</button>
      </div>
    </header>

    <main class="main-sections">
      <About />
      <Testimonial />
      <ContactUs />
    </main>

    <FooTer />
  </div>
</template>

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
      heading: 'Welcome to Our Platform!',
      description: 'Explore a modern Vue.js experience built with simplicity and professionalism.',
      buttonText: 'Get Started'
    };
  },
  methods: {
    sayhello() {
      alert('Thanks for showing interest!');
    }
  }
};
</script>

<style scoped>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.app-container {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f8fafc; /* slate-50 */
  color: #0f172a;
  min-height: 100vh;
}

.hero {
  background: linear-gradient(to right, #3b82f6, #60a5fa);
  color: white;
  padding: 4rem 1.5rem;
  text-align: center;
  border-radius: 0.5rem;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
  margin: 2rem 1rem;
}

.hero-content {
  max-width: 700px;
  margin: 0 auto;
}

.hero h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.hero p {
  font-size: 1.125rem;
  margin-bottom: 2rem;
  opacity: 0.9;
}

.cta-button {
  background-color: white;
  color: #3b82f6;
  border: none;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  border-radius: 0.375rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.cta-button:hover {
  background-color: #e0e7ff;
  color: #1d4ed8;
}

.main-sections {
  padding: 2rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 3rem;
}
</style>
