<script setup>
const props = defineProps(["title"]);
</script>

<template>
  <div class="card">
    <h2>{{ props.title }}</h2>
  </div>
</template>

<style scoped>
.card {
  width: 100%;
  max-width: 600px;
  padding: 1.2rem;
  border-radius: 0.6rem;
  background-color: #54595f;
  color: white;
  text-align: center;
  transition: all ease 0.25s;
}

.card:hover {
  background-color: #407877;
  cursor: pointer;
}
</style>
