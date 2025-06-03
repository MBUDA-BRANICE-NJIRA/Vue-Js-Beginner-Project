<!-- Testimonials.vue -->
<template>
  <section class="testimonials">
    <h2 class="section-title">Intresting Views And Testimonials</h2>
    <div class="testimonial-card" v-for="(testimonial, index) in testimonials" :key="index">
      <p class="quote">"{{ testimonial.message }}"</p>
      <p class="author">— {{ testimonial.name }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TestiMonial',
  data() {
    return {
      testimonials: [
        { name: 'Alice', message: 'This app is amazing!' },
        { name: 'Bob', message: 'I love using it every day.' },
        { name: 'Carol', message: 'Highly recommend to everyone.' }
      ]
    };
  }
};
</script>

<style scoped>
.testimonials {
  background-color: #f8fafc;
  padding: 2rem;
  text-align: center;
  border-radius: 0.5rem;
}

.section-title {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  color: #1e293b;
}

.testimonial-card {
  background-color: #e2e8f0;
  margin: 1rem auto;
  padding: 1rem;
  border-radius: 0.375rem;
  max-width: 400px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.quote {
  font-style: italic;
  color: #334155;
}

.author {
  margin-top: 0.5rem;
  font-weight: bold;
  color: #0f172a;
}
</style>
