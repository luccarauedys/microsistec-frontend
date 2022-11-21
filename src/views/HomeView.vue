<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <main>
    <h1>Início</h1>
    <div class="cards">
      <Card title="Cadastrar clientes" />
      <Card title="Buscar clientes" />
      <Card title="Cadastrar imóveis" />
      <Card title="Buscar imóveis" />
    </div>
  </main>
</template>

<style scoped>
main {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.cards {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

@media (max-width: 650px) {
  .cards {
    grid-template-columns: 1fr;
  }
}
</style>
