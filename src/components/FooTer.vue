<!-- Footer.vue -->
<template>
  <footer class="footer">
    <p>&copy; {{ new Date().getFullYear() }} My Vue App. All rights reserved.</p>
  </footer>
</template>

<script>
export default {
  name: 'FooTer',
};
</script>

<style scoped>
.footer {
  background-color: #1e293b;
  color: #f8fafc; 
  text-align: center;
  padding: 1rem;
  font-size: 0.9rem;
  margin-top: auto;
}
</style>
