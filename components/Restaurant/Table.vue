<script setup>
import topItems from "../../data.json";
const tops = ref([]);
const organizedRestauranst = reactive({
  first: [...topItems].splice(0, 25),
  second: [...topItems].splice(25, 50),
});
</script>

<template>
  <div>
    <div class="wrapper">
      <h1 class="table-title">Top 50:The Ranking</h1>
      <div class="table-container">
        <div class="table-item">
          <RestaurantRow :top-restaurants="organizedRestauranst.first" />
        </div>

        <div class="table-item">
          <RestaurantRow :top-restaurants="organizedRestauranst.second" />
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
div.wrapper {
  margin: 2rem auto;
  max-width: 900px;
  text-align: center;
}
.table-title {
  font-weight: bold;
  font-size: 2em;
  font-family: Arial, Helvetica, sans-serif;
}
.table-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  padding: 2rem;
}
.table-item {
  display: flex;
  flex-direction: column;
  flex: 0.5;
  margin-right: 2rem;
}
</style>
