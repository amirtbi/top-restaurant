<template>
  <div>
    <slot />
    <RestaurantAd />
  </div>
</template>
<style scoped>
div.ad-container {
  display: flex;
  flex-direction: column;
  background-color: indigo;
  color: white;
  width: 100%;
  padding: 2rem;
  align-items: center;
}
p {
  font-family: Arial, Helvetica, sans-serif;
}
button {
  background-color: green;
  border: none;
  padding: 0.75rem 2rem;
  color: white;
  border-radius: 12px;
  width: 120px;
  margin-top: 1rem;
}
</style>
