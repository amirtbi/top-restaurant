<template>
  <div class="table-header">
    <h4>Rank</h4>
    <h4>Chain</h4>
  </div>
</template>

<style scoped>
.table-header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  border-top: 1px solid #ccc;
}
.table-header > h4 {
  text-align: left;
  flex: 0.5;
  padding: 0.2rem;
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
  color: green;
}
</style>
