<template>
  <div class="card">
    {{ title }}
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ['title'],
}
</script>

<style scoped>
.card {
  margin-bottom: 10px;
  padding: 10px;
  background-color: gray;
  cursor: pointer;
}
</style>