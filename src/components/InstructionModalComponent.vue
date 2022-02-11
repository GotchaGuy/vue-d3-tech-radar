<template>
  <section v-if="displayed" class="sidebar-modal-component p-6 fixed bg-mvp-gray-darker w-2/5">
    <div class="flex justify-between pb-6">
      <h3 class="text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB 3</span> Technology radar </h3>
      <button @click="displayed = false" class="x-button text-gray-300 hover:text-gray-100">
        <svg
            class="x-button-icon"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
        >
          <path
              strokeLinecap="round"
              strokeLinejoin="round"
              strokeWidth={2}
              d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
    </div>
    <h2 class="text-4xl font-bold"> What is Web3 tech radar and how to read it? </h2>
    <div class="about-info pb-6">

    </div>
    <div class="info-accordion pb-6">

    </div>
  </section>

</template>


<script>

export default {
  name: "InstructionModal",
  components: {},
  props: {},
  data() {
    return {
      displayed: false,

    }
  },
  mounted() {
    this.emitter.on("toggle-instruction-modal", (data) => {
      this.displayed = data.displayed;
    });
  },
  methods: {},

}
</script>

