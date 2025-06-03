<template>
  <section class="about-section">
    <div class="about-container">
      <div class="about-text">
        <h2 class="about-title">About Us</h2>
        <p class="about-description">
          Welcome to our Vue.js application! We're a passionate team committed to crafting clean, intuitive, and high-performance web solutions.
        </p>
        <p class="about-description">
          With expertise in frontend frameworks like Vue and React, and a deep love for UI/UX, we build web experiences that are scalable, efficient, and user-centered. Whether you're a developer, business, or creative — you're in the right place.
        </p>
      </div>
      <div class="about-image-wrapper">
        <img
          src="https://i.pravatar.cc/100?img=1"
          alt="Team working on tech"
          class="about-image"
        />
      </div>
    </div>
  </section>
</template>


<script>
export default {
  name: 'AbouT'
};
</script>

<style scoped>
.about-section {
  background-color: #f8fafc;
  padding: 4rem 1.5rem;
}

.about-container {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  max-width: 1100px;
  margin: 0 auto;
  align-items: center;
  justify-content: center;
}

@media (min-width: 768px) {
  .about-container {
    flex-direction: row;
    align-items: flex-start;
  }
}

.about-text {
  max-width: 600px;
}

.about-title {
  font-size: 2rem;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 1rem;
}

.about-description {
  font-size: 1.125rem;
  color: #475569;
  line-height: 1.75;
  margin-bottom: 1rem;
}

.about-image-wrapper {
  flex-shrink: 0;
}

.about-image {
  width: 100%;
  max-width: 500px;
  border-radius: 0.75rem;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.08);
  object-fit: cover;
}
</style>
