<template>
  <section class="grid place-items-center relative">
    <!-- District Map -->
    <div class="w-full h-full">
      <img src="../images/map.png" alt="building-map" />
    </div>

    <!-- Cameras -->
    <!-- camera 01 -->
    <button class="camera one group">
      01<span class="tooltip tip-one">View 01</span>
    </button>
    <div class="view01"></div>

    <!-- camera 02 -->
    <button class="camera two group">
      02<span class="tooltip tip-two">View 02</span>
    </button>

    <!-- camera 03 -->
    <button class="camera three group">
      03<span class="tooltip tip-three">View 03</span>
    </button>

    <!-- camera 04 -->
    <button class="camera four group">
      04<span class="tooltip tip-four">View 04</span>
    </button>
  </section>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style>
.view01 {
  background: black;
  opacity: 0.5;
  clip-path: polygon(0 0, 100% 0, 100% 56%, 76% 34%, 62.3% 100%, 0 100%);
}
</style>
