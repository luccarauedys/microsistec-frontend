<script setup>
import { useRouter } from "vue-router";
import Card from "@/components/Card.vue";

const router = useRouter();
</script>

<template>
  <main>
    <h1>Sistema de admin</h1>
    <div class="cards">
      <Card title="Cadastrar clientes" @click="router.push('/clientes')" />
      <Card title="Buscar clientes" @click="router.push('/clientes')" />
      <Card title="Cadastrar imóveis" @click="router.push('/imoveis')" />
      <Card title="Buscar imóveis" @click="router.push('/imoveis')" />
    </div>
  </main>
</template>

<style scoped>
h1 {
  text-align: center;
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
