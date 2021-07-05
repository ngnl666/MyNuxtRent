<template>
  <!-- 自訂樣板(避免 dry) -->
  <div>
    <div class="container">
      <NuxtLink to="/">Go Back</NuxtLink>
    </div>
    <Nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  padding-top: 6rem;
  margin-bottom: -5rem;
}
</style>
