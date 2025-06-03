<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-brand">
        <h2>My Vue App</h2>
        <p>Building modern web experiences with Vue.js.</p>
      </div>

      <div class="footer-links">
        <a href="#">More</a>
        <a href="#">Projects</a>
        <a href="#">Opportunities</a>
        <a href="#">Privacy</a>
      </div>
    </div>

    <div class="footer-bottom">
      <p>&copy; {{ currentYear }} My Vue App. All rights reserved.</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooTer',
  computed: {
    currentYear() {
      return new Date().getFullYear();
    }
  }
};
</script>

<style scoped>
.footer {
  background-color: #1e293b; /* slate-800 */
  color: #f8fafc; /* slate-50 */
  padding: 2rem 1rem 1rem;
  font-size: 0.95rem;
}

.footer-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
  text-align: center;
}

.footer-brand h2 {
  margin: 0;
  font-size: 1.25rem;
  color: #3b82f6;
}

.footer-brand p {
  margin: 0.25rem 0 0;
  color: #cbd5e1;
  font-size: 0.95rem;
}

.footer-links {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}

.footer-links a {
  color: #f8fafc;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: #3b82f6;
}

.footer-bottom {
  border-top: 1px solid #334155; /* slate-700 */
  margin-top: 2rem;
  padding-top: 1rem;
  font-size: 0.85rem;
  color: #94a3b8; /* slate-400 */
}
</style>
