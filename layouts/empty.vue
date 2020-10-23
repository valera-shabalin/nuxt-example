<template>
  <div class="empty-layout">
    <nuxt />
  </div>
</template>

<script>
  export default {
    name: 'EmptyLayout'
  }
</script>

<style>
  .empty-layout {
    display: flex;
    justify-content: center;
    padding-top: 5rem;
  }
</style>
