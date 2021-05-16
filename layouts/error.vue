<template>
  <div>
    <h1 v-if="error.statusCode === 404">Página não encontrada</h1>
    <h1 v-else>Parece que um erro aconteceu.</h1>
    <NuxtLink to="/">Voltar ao início</NuxtLink>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error' // you can set a custom layout for the error page
  }
</script>
