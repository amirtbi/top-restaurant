<script setup>
const homeIsActive = ref(true);
const otherLinkIsActive = ref(false);
const setActiveClass = (item) => {
  if (item === "Home") {
    homeIsActive.value = true;
    otherLinkIsActive.value = false;
  } else {
    homeIsActive.value = false;
    otherLinkIsActive.value = true;
  }
};
</script>

<template>
  <nav class="flex w-1/2 justify-end">
    <ul class="flex items-center justify-between">
      <li
        @click="setActiveClass('Home')"
        :class="{ 'text-green-400': homeIsActive }"
        class="cursor-pointer text-white text-xl font-bold p-2 hover:text-gray-300"
      >
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li
        :class="{ 'text-green-400': otherLinkIsActive }"
        @click="setActiveClass('Restaurants')"
        class="cursor-pointer text-white text-xl font-bold p-2 hover:text-gray-300"
      >
        <NuxtLink to="/restaurants">Restaurants</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped></style>
