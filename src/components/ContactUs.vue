<template>
  <section class="contact">
    <div class="container">
      <h2 class="title">Contact Us</h2>
      <p class="subtitle">We’d love to hear from you! Please fill out the form below.</p>

      <form @submit.prevent="handleSubmit" class="form">
        <div class="form-group">
          <label for="name">Name</label>
          <input v-model="form.name" type="text" id="name" required />
        </div>

        <div class="form-group">
          <label for="email">Email</label>
          <input v-model="form.email" type="email" id="email" required />
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea v-model="form.message" id="message" rows="4" required></textarea>
        </div>

        <button type="submit" class="submit-button">Send</button>
        <p v-if="submitted" class="success">Thank you! We’ll get back to you soon.</p>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactUs',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    };
  },
  methods: {
    handleSubmit() {
      console.log('Message sent:', this.form);
      this.submitted = true;
      this.form = { name: '', email: '', message: '' };
    }
  }
};
</script>

<style scoped>
.contact {
  background-color: #f1f5f9;
  padding: 3rem 1.5rem;
  text-align: center;
}

.container {
  background: white;
  padding: 2rem;
  border-radius: 0.5rem;
  max-width: 600px;
  margin: auto;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}

.title {
  font-size: 2rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
}

.subtitle {
  color: #475569;
  margin-bottom: 2rem;
  font-size: 1rem;
}

.form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.form-group {
  text-align: left;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  color: #334155;
  font-weight: 500;
}

input,
textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #cbd5e1;
  border-radius: 0.375rem;
  font-size: 1rem;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3b82f6;
  box-shadow: 0 0 0 2px rgba(59, 130, 246, 0.2);
}

.submit-button {
  padding: 0.75rem 1.5rem;
  background-color: #3b82f6;
  color: white;
  border: none;
  border-radius: 0.375rem;
  cursor: pointer;
  font-weight: 600;
  transition: background-color 0.3s ease;
}

.submit-button:hover {
  background-color: #2563eb;
}

.success {
  color: #16a34a;
  margin-top: 1rem;
  font-weight: 500;
}
</style>
