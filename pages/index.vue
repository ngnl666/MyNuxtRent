<template>
  <div>
    <div class="container">
      <!-- auto import components (detail at nuxt.config.js)-->
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
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
      smallCardSections
    };
  }
};
</script>
