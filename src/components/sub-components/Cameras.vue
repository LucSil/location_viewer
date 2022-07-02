<template>
  <!-- Cameras -->
  <!-- camera 01 -->
  <button
    v-if="one"
    class="camera one group"
    @click="$emit('viewImg', $event.target)"
    @mouseenter="showView"
    @mouseleave="hideView"
  >
    01<span class="tooltip tip-one">View 01</span>
  </button>
  <div class="view01" v-if="view01"></div>

  <!-- camera 02 -->
  <button
    v-if="two"
    class="camera two group"
    @click="$emit('viewImg', $event.target)"
    @mouseenter="showView"
    @mouseleave="hideView"
  >
    02<span class="tooltip tip-two">View 02</span>
  </button>
  <div class="view02" v-if="view02"></div>

  <!-- camera 03 -->
  <button
    v-if="three"
    class="camera three group"
    @click="$emit('viewImg', $event.target)"
    @mouseenter="showView"
    @mouseleave="hideView"
  >
    03<span class="tooltip tip-three">View 03</span>
  </button>
  <div class="view03" v-if="view03"></div>

  <!-- camera 04 -->
  <button
    v-if="four"
    class="camera four group"
    @click="$emit('viewImg', $event.target)"
    @mouseenter="showView"
    @mouseleave="hideView"
  >
    04<span class="tooltip tip-four">View 04</span>
  </button>
  <div class="view04" v-if="view04"></div>
</template>

<script>
export default {
  name: "Cameras",
  emits: ["viewImg"],
  data() {
    return {
      // Camera Icons
      one: true,
      two: true,
      three: true,
      four: true,

      // Camera Views
      view01: false,
      view02: false,
      view03: false,
      view04: false,
    };
  },

  methods: {
    showView: function (e) {
      let one = document.querySelector(".one");
      let two = document.querySelector(".two");
      let three = document.querySelector(".three");
      let four = document.querySelector(".four");

      if (e.target == one) {
        this.view01 = true;
        this.two = false;
        this.three = false;
        this.four = false;
      } else if (e.target == two) {
        this.view02 = true;
        this.one = false;
        this.three = false;
        this.four = false;
      } else if (e.target == three) {
        this.view03 = true;
        this.one = false;
        this.two = false;
        this.four = false;
      } else if (e.target == four) {
        this.view04 = true;
        this.one = false;
        this.two = false;
        this.three = false;
      }
    },

    hideView: function (e) {
      let one = document.querySelector(".one");
      let two = document.querySelector(".two");
      let three = document.querySelector(".three");
      let four = document.querySelector(".four");

      if (e.target == one) {
        this.view01 = false;
        this.two = true;
        this.three = true;
        this.four = true;
      } else if (e.target == two) {
        this.view02 = false;
        this.one = true;
        this.three = true;
        this.four = true;
      } else if (e.target == three) {
        this.view03 = false;
        this.one = true;
        this.two = true;
        this.four = true;
      } else if (e.target == four) {
        this.view04 = false;
        this.one = true;
        this.two = true;
        this.three = true;
      }
    },
  },
};
</script>

<style>
.view01 {
  clip-path: polygon(0 0, 100% 0, 100% 56%, 76% 34%, 62.3% 100%, 0 100%);
}
.view02 {
  clip-path: polygon(0 0, 35% 0, 56% 44%, 80% 0, 100% 0, 100% 100%, 0 100%);
}
.view03 {
  clip-path: polygon(0 0, 74% 0, 50% 72%, 100% 36%, 100% 100%, 0 100%);
}
.view04 {
  clip-path: polygon(
    0 0,
    100% 0,
    100% 40%,
    30% 53.5%,
    100% 85%,
    100% 100%,
    0 100%
  );
}
</style>
