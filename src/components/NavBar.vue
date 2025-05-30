<template>
  <nav class="navbar">
    
    <ul class="nav-list">
      <li class="nav-item"><a href="/">Home</a></li>
      <li class="nav-item"><a href="/about">About</a></li>
      <li class="nav-item"><a href="/contact">Contact</a></li>
      <li class="nav-item"><a href="/services">Services</a></li>
      <li class="nav-item"><a href="/blog">Blog</a></li>
      <li class="nav-item"><a href="/faq">FAQ</a></li>
      <li class="nav-item"><a href="/login">Login</a></li>

    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
};
</script>

<style scoped>
.navbar {
  background-color: #1e293b; /* slate-800 */
  padding: 1rem;
  
}

.nav-list {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
  justify-content: center;
}

.nav-item a {
  color: #f8fafc; /* slate-50 */
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-item a:hover {
  color: #38bdf8; /* sky-400 */
}
</style>
