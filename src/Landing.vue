<template>
  <section id="landing" class="h-screen bg-mvp-gray-dark">
    <div class="h-screen container-sm flex flex-col items-center justify-center text-center relative">

    <div class="logo mb-16 absolute top-8 xl:top-16">
      <img class="w-24" src="./assets/svg/3327logo-multicolor.svg" alt="3327 logo">
    </div>

    <h1 class="text-5xl lg:text-7xl font-sans font-bold mb-2 lg:mb-5 lg:mt-0">WEB3</h1>
      <h2 class="text-5xl lg:text-7xl font-normal mb-5"> Technology radar </h2>
    <p class="mb-5 p-5 w-full lg:w-1/3">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
      feugiat sapien sem, quis sollicitudin sapien congue sit amet.</p>
    <p class="mb-5">Current version - <span class="font-bold">5 (02 2022)</span></p>
    <a
        class="flex align-middle justify-center items-center my-5 px-10 py-1 button filter-button-active rounded-full mb-2">
      <span class="leading-6 text-xl font-bold"> Check it out </span>

    </a>
    </div>
  </section>

</template>

<script>
export default {
  name: "Landing",
  components: {},
  props: {},
  data() {
    return {}
  },
  mounted() {
  },
  methods: {
    methodHere() {
    },
  },

}
</script>

<style scoped>
/*#landing::after {*/
/*  content: "";*/
/*  background-image: url("./assets/svg/full-screen-circles.svg");*/
/*  position:absolute;*/
/*  top:0;*/
/*  width: 100vh;*/
/*  height: 100vh;*/
/*}*/


</style>

