<script setup>
import { RouterLink, RouterView } from "vue-router";
import LogoMicrosistec from "@/assets/images/logo-microsistec.png";
</script>

<template>
  <header>
    <img :src="LogoMicrosistec" />
    <nav>
      <RouterLink to="/">Início</RouterLink>
      <RouterLink to="/clientes">Clientes</RouterLink>
      <RouterLink to="/imoveis">Imóveis</RouterLink>
    </nav>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 2rem;
  background-color: #3f7877;
  color: white;
}

img {
  height: 2.2rem;
  cursor: pointer;
}

nav {
  display: flex;
  gap: 0.2rem;
}

a {
  color: white;
  text-decoration: none;
  font-size: 1.2rem;
  padding: 0.5rem 1rem;
  border-radius: 0.3rem;
  transition: all ease 0.25s;
}

a:hover {
  background-color: #54595f;
}

@media (max-width: 650px) {
  header {
    flex-direction: column;
    gap: 2rem;
  }
}
</style>
