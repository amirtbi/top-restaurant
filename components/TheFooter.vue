<template>
  <div class="footer-container">
    <footer>
      <h1>Welcome to Restaurant page</h1>
      <nuxt-link to="/">Go to Home</nuxt-link>
    </footer>
  </div>
</template>
<style scoped>
div.footer-container {
  display: flex;
  width: 100%;
  height: 120px;
  max-height: 120px;

  background-color: rgb(72, 149, 72);
  color: white;
  margin-top: 20px;
}
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
h1 {
  color: white;
  font-size: 2rem;
  text-align: center;
}
</style>
