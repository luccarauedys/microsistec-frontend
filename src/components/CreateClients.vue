<script setup>
import { ref } from "vue";

const name = ref("");
const contact = ref({ type: "", contact: "" });
const errorMessage = ref("");

function handleSubmit(e) {
  e.preventDefault();

  if (!name || !contact.type || !contact.contact) {
    errorMessage.value = "Por favor, preencha todos os campos!";
  }

  const client = {
    name: name.value,
    contacts: [contact.value],
  };

  // TODO: enviar dados pra api
}
</script>

<template>
  <div>
    <h1>Cadastro de clientes</h1>

    <form :onsubmit="handleSubmit">
      <p>Nome do cliente</p>

      <input v-model="name" placeholder="Nome do cliente" required />

      <p>Informações de contato</p>

      <select v-model="contact.type" required>
        <option disabled value="">Selecione o tipo de contato</option>
        <option>Telefone</option>
        <option>Email</option>
      </select>

      <input v-model="contact.contact" placeholder="Contato do cliente" required />

      <p :v-if="errorMessage" class="error">{{ errorMessage }}</p>
      <button type="submit">Cadastrar cliente</button>
    </form>
  </div>
</template>

<style scoped>
*:not(h1) {
  font-size: 1.1rem;
}

h1 {
  text-align: center;
}

form {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  max-width: 400px;
  margin: 1rem auto;
}

form p {
  font-weight: 500;
}

input,
select,
option,
button {
  padding: 0.5rem;
}

.error {
  color: red;
  font-size: 0.8rem;
}

button {
  font-weight: bold;
  padding: 1rem;
  border-radius: 0.3rem;
  background-color: #7a3bd0;
  color: white;
  transition: all ease 0.3s;
}

button:hover {
  background-color: #6b32ba;
  cursor: pointer;
}
</style>
