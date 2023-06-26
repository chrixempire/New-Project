<template>
  <div>
    <div class="container">
      <Heroes />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import Heroes from "~/components/Heroes";
import { largeCardSections, smallCardSections } from "@/assets/data.js";
import LargeCardDisplay from "~/components/LargeCardDisplay";
import SmallCardDisplay from "~/components/SmallCardDisplay";

export default {
  layout: "appLayout",
  components: { Heroes, LargeCardDisplay, SmallCardDisplay },
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    };
  },
};
</script>
