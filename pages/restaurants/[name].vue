<script setup>
import restaurant from "../../data.json";
const foundRestaurant = ref({});
const route = useRoute();
const routeName = computed(() => {
  return route.params.name;
});
const result = restaurant.find((r) => {
  if (r.name === routeName.value) {
    return r;
  }
});
foundRestaurant.value = result;
</script>

<template>
  <div>
    <NuxtLayout name="custom" v-if="!!foundRestaurant">
      <div class="restaurant-container">
        <div class="image-container">
          <img :src="foundRestaurant.imageUrl" alt="" />
        </div>
        <div class="info-container">
          <h1>{{ foundRestaurant.name }}</h1>
          <div class="stats-container">
            <h5>Revenue (in billions)</h5>
            <p>${{ foundRestaurant.revenue }}</p>
          </div>
          <div class="stats-container">
            <h5>Number of Stores</h5>
            <p>{{ foundRestaurant.numberOfStores }}</p>
          </div>
          <p class="content">{{ foundRestaurant.content }}</p>
        </div>
      </div>
    </NuxtLayout>
    <NuxtLayout name="error" v-else>
      <template #error-text>Not found restaurants</template>
      <template #redirectEl>
        <NuxtLink to="/restaurants">Go Back</NuxtLink>
      </template>
    </NuxtLayout>
  </div>
</template>
<style scoped>
.restaurant-container {
  display: flex;
}
.image-container {
  width: 75%;
  height: 95vh;
}
.image-container img {
  width: 100%;
  height: 100%;
}
.restaurant-not-found {
  height: 75vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.info-container {
  padding: 3rem;
  width: 50%;
}
.info-container h1 {
  text-transform: uppercase;
  font-size: 6rem;
  margin-bottom: 3rem;
}
.stats-container {
  display: flex;
  align-items: flex-end;
  margin-bottom: 1rem;
}
.stats-container h5 {
  width: 20rem;
  font-size: 2rem;
  margin: 0;
  margin-right: 5rem;
}
.stats-container p {
  font-size: 2rem;
  margin: 0;
}
.content {
  font-size: 1.5rem;
  margin-top: 4rem;
}
img {
  width: 10rem;
}
.notFound-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 4rem;
}
.notFound-container > h2 {
  font-size: 3rem;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
}
.notFound-container > button {
  background-color: rgb(157, 157, 206);
  padding: 0.75rem 1.5rem;
  color: white;
}
</style>
