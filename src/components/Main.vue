<template>
  <section class="grid place-items-center relative">
    <!-- District Map -->
    <div class="w-full h-full">
      <img src="../images/map.png" alt="building-map" />
    </div>

    <!-- Cameras -->
    <button class="camera one group">
      01<span class="tooltip tip-one">View 01</span>
    </button>
    <button class="camera two group">
      02<span class="tooltip tip-two">View 02</span>
    </button>
    <button class="camera three group">
      03<span class="tooltip tip-three">View 03</span>
    </button>
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
