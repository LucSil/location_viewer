<template>
  <section class="grid place-items-center relative">
    <!-- District Map -->
    <div class="w-full h-full">
      <img src="../images/map.png" alt="building-map" />
    </div>

    <!-- Cameras -->
    <Cameras />

    <!-- Image section -->
    <div
      v-if="images"
      class="absolute bottom-0 left-0 w-56 border-2 border-amber-500"
    >
      <img :src="require(`../${images}`)" alt="" />
    </div>
  </section>
</template>

<script>
import Cameras from "@/components/sub-components/Cameras.vue";
export default {
  name: "Main",
  components: { Cameras },
};
</script>
