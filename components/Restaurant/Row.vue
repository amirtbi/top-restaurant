<script setup>
const props = defineProps({
  topRestaurants: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <!-- row header-->
  <RestaurantHeader />
  <div
    class="table-rows"
    v-for="(item, index) in topRestaurants"
    :class="{ evenRowColor: (index + 1) % 2 === 0 }"
    :key="item.id"
  >
    <h4>{{ item.rank }}</h4>
    <h4>
      <NuxtLink :to="`/restaurants/${item.name}`">{{ item.name }}</NuxtLink>
    </h4>
  </div>
</template>

<style scoped>
.table-rows {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  border-top: 1px solid darkgray;
  background-color: rgb(54, 54, 54);
  color: black;
  padding: 0.5rem;
}
.table-rows > h4 {
  text-align: left;
}
.table-rows > h4:first-of-type {
  flex: 0.2;
}
.table-rows > h4:last-of-type {
  flex: 0.8;
  text-align: center;
}
.table-rows > h4:first-of-type {
  font-weight: bold;
}
h4 > a,
h4 {
  color: rgb(10, 163, 10);
}
.evenRowColor {
  background-color: rgba(19, 15, 15);
}
</style>
