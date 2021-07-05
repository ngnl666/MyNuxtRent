<template>
  <div class="container">
    <MyItem v-for="rental in myRentals" :key="rental.id" :item="rental" />
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  layout: "no-nav", // 跳到指定的 layout (.nuxt/layouts/no-nav.vue)
  computed: {
    ...mapState(["myRentals"])
  }
};
</script>

<style scoped></style>
