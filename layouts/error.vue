<template>
  <div>
    <h1>
      <slot name="error-text"></slot>
    </h1>
    <div class="image-container">
      <img
        src="http://cdn.shopify.com/s/files/1/1061/1924/products/Very_sad_emoji_icon_png_grande.png?v=1571606089"
        alt=""
      />
    </div>
    <div class="action-container">
      <slot name="redirectEl"></slot>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1.5rem;
  font-weight: bold;
  text-align: center;
  padding: 1.5rem;
}
div.image-container {
  display: flex;
  max-width: 100px;
  margin: 2rem auto;
}
img {
  width: 100%;
  max-width: 100%;
}
.action-container {
  display: flex;
  justify-content: center;
  flex-direction: row;
}
button {
  background-color: blue;
  color: white;
  padding: 0.75rem 2rem;
  border-radius: 2rem;
}
</style>
