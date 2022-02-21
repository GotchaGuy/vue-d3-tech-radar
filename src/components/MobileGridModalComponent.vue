<template>
  <section v-if="displayed"
           class="sidebar-modal-component h-screen w-full h-screen bg-mvp-gray-darker overflow-auto fixed bottom-0 z-5">
    <div class="md:hidden p-6 h-32">
      <h3 class="md:inline-block hidden text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB 3</span> Technology radar </h3>

    </div>
    <div class="p-6 bg-mvp-gray-darker h-full">
      <Grid/>
    </div>
  </section>
</template>

<script>
import Grid from './GridComponent.vue'

export default {
  name: "MobileGridModal",
  components: {
    Grid,
  },
  props: {},
  data() {
    return {
      displayed: false,
    }
  },
  mounted() {
    this.emitter.on("toggle-mobile-grid-modal", (data) => {
      this.displayed = data.displayed;
    });
  }
}
</script>
