<template>
  <section class="about">
    <div class="content">
      <h2 class="title">About Us</h2>
      <p class="description">
        Welcome to our Vue.js application! We’re a passionate team dedicated to building clean, modern, and user-friendly web experiences.
        Our goal is to make web apps that are both functional and enjoyable to use.
      </p>
      <p class="description">
        We specialize in frontend development, UI/UX design, and building scalable solutions with Vue, React, and modern web technologies.
        Whether you're a developer, designer, or business owner — there's something for you here!
      </p>
    </div>
    <img src="https://source.unsplash.com/500x300/?technology,team" alt="About illustration" class="about-image" />
  </section>
</template>

<script>
export default {
  name: 'About'
};
</script>

<style scoped>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 3rem 1rem;
  background-color: #f1f5f9;
  border-radius: 0.5rem;
  text-align: center;
}

@media (min-width: 768px) {
  .about {
    flex-direction: row;
    justify-content: space-between;
    text-align: left;
  }
}

.content {
  max-width: 600px;
}

.title {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #1e293b;
  font-weight: bold;
}

.description {
  font-size: 1rem;
  color: #475569;
  margin-bottom: 1rem;
  line-height: 1.6;
}

.about-image {
  width: 100%;
  max-width: 500px;
  border-radius: 0.5rem;
  margin-top: 2rem;
}

@media (min-width: 768px) {
  .about-image {
    margin-top: 0;
    margin-left: 2rem;
  }
}
</style>
