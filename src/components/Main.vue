<template>
  <section class="grid place-items-center relative">
    <!-- District Map -->
    <div class="w-full h-full">
      <img src="../images/map.png" alt="building-map" />
    </div>

    <!-- Cameras -->
    <Cameras />
  </section>
</template>

<script>
import Cameras from "@/components/sub-components/Cameras.vue";
export default {
  name: "Main",
  components: { Cameras },
};
</script>
