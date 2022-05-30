<template>
  <div>
    <NuxtLayout name="error">
      <template #error-text>Page not found!</template>
      <template #redirectEl>
        <NuxtLink to="/">Go Home</NuxtLink>
      </template>
    </NuxtLayout>
  </div>
</template>
<style scoped>
.main-container {
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
  align-items: center;
  margin: 2rem auto;
  width: 100%;
  font-weight: bold;
  font-size: 2rem;
}
a {
  color: rgb(68, 68, 198);
}
a:hover {
  text-decoration: underline;
}
</style>
