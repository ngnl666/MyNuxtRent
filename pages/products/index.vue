<template>
  <!-- index.vue 會作為資料夾名的 '預設路由' (/products) -->
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "/static/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    };
  }
};
</script>

<style scoped></style>
