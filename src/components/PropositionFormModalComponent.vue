<template>
  <section v-if="displayed" class="sidebar-modal-component p-6 fixed bg-mvp-gray-darker w-2/5">
    <div class="flex justify-between pb-6">
      <h3 class="text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB 3</span> Technology radar</h3>
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
    <h2 class="text-4xl font-bold"> Propose tech you would like to see on the radar </h2>
    <div class="about-info pb-6">
      <p class="text-sm py-2 text-gray-300 font-light">The acronym zk-SNARK stands for "Zera-Knowledge Succinet
        Non-Interactive Argument of
        Knowledge," and refers to a proot construction where ane can prave passesaion of certain
        information, e.g. a secret key, without revealing that information, and without any interaction
        between the praver and verifier.
      </p>
    </div>
    <div class="proposition-form pb-6 w-96">
      <form action="" class="w-full">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required type="text" placeholder="Project or technology name">
        <select class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required name="category" id="category" placeholder="Category">
          <option value="tools">Tools</option>
          <option value="tools">Tools</option>
          <option value="tools">Tools</option>
          <option value="tools">Tools</option>
        </select>
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required type="url" placeholder="Official project website or repository">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" type="text" placeholder="Project twitter account (optional)">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" type="text" placeholder="Your twitter account if you want shout out (optional)">
        <button
            class="flex align-middle justify-center items-center mt-4 px-2 py-1 button filter-button-active rounded-full mb-2">
          <span class="leading-6 text-base font-bold"> Submit proposal </span>
        </button>
      </form>
    </div>
  </section>

</template>


<script>

export default {
  name: "PropositionFormModal",
  components: {},
  props: {},
  data() {
    return {
      displayed: false,

    }
  },
  mounted() {
    this.emitter.on("toggle-proposition-form-modal", (data) => {
      this.displayed = data.displayed;
    });
  },
  methods: {},

}
</script>

<style>
    input:focus, textarea:focus, select:focus{
        outline: none;
    }
</style>

