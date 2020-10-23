<template>
  <section>
    <h1>{{user.name}}</h1>
    <hr>
    <h3>{{user.email}}</h3>
  </section>
</template>

<script>
  export default {
    name: 'UserId',
    validate({ params }) {
      return /^\d+$/.test(params.id)
      //return true // если true, то можно зайти на данную страницу
    },
    async asyncData({ $axios, params }) {
      const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
      return { user }
    }
  }
</script>

<style>

</style>
