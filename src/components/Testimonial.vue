<template>
  <section class="testimonials">
    <h2 class="section-title">Interesting Views & Testimonials</h2>
    <div class="card-grid">
      <div class="testimonial-card" v-for="(testimonial, index) in testimonials" :key="index">
        <img :src="testimonial.avatar" alt="User avatar" class="avatar" />
        <p class="quote">"{{ testimonial.message }}"</p>
        <p class="author">— {{ testimonial.name }}</p>
        <p class="role">{{ testimonial.role }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TestiMonials',
  data() {
    return {
      testimonials: [
        {
          name: 'Alice Johnson',
          message: 'This app is absolutely incredible. The user experience is top notch!',
          role: 'Product Manager at TechCorp',
          avatar: 'https://i.pravatar.cc/100?img=1'
        },
        {
          name: 'Bob Smith',
          message: 'I use this platform daily, and it has streamlined my work completely.',
          role: 'Freelance Developer',
          avatar: 'https://i.pravatar.cc/100?img=2'
        },
        {
          name: 'Carol Danvers',
          message: 'Professional, clean, and easy to use. Highly recommended!',
          role: 'UX Designer at DesignFlow',
          avatar: 'https://i.pravatar.cc/100?img=3'
        }
      ]
    };
  }
};
</script>

<style scoped>
.testimonials {
  background-color: #f8fafc;
  padding: 3rem 1rem;
  text-align: center;
}

.section-title {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #1e293b;
  font-weight: 600;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
  max-width: 1000px;
  margin: 0 auto;
}

.testimonial-card {
  background-color: white;
  border-radius: 0.75rem;
  padding: 2rem 1.5rem;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.testimonial-card:hover {
  transform: translateY(-5px);
}

.avatar {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 1rem;
}

.quote {
  font-style: italic;
  color: #475569;
  margin-bottom: 1rem;
}

.author {
  font-weight: 600;
  color: #0f172a;
}

.role {
  font-size: 0.85rem;
  color: #64748b;
}
</style>
