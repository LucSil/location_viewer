<template>
  <section class="grid place-items-center relative">
    <!-- District Map -->
    <div class="w-full h-full">
      <img src="../images/map.png" alt="building-map" />
    </div>

    <!-- Cameras -->
    <Cameras @viewImg="viewImg" />

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
import mainData from "@/data.json";
import Cameras from "@/components/sub-components/Cameras.vue";
export default {
  name: "Main",
  components: { Cameras },
  data() {
    return {
      images: false,
    };
  },
  methods: {
    viewImg: function (target) {
      let one = document.querySelector(".one");
      let two = document.querySelector(".two");
      let three = document.querySelector(".three");
      let four = document.querySelector(".four");
      if (target == one) {
        this.images = mainData.images.one;
      } else if (target == two) {
        this.images = mainData.images.two;
      } else if (target == three) {
        this.images = mainData.images.three;
      } else if (target == four) {
        this.images = mainData.images.four;
      }
    },
  },
};
</script>
