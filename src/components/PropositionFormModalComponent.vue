<template>
  <section v-if="displayed" class="sidebar-modal-component h-screen sm:w-full md:w-2/5 bg-mvp-gray-darker overflow-auto fixed bottom-0">
    <div class="md:hidden p-6 bg-gray-200 opacity-40 h-32"></div>
  <div class="p-6 bg-mvp-gray-darker h-full">
    <div class="flex justify-between items-start">
      <h3 class="md:inline-block hidden text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB 3</span> Technology radar</h3>
      <h2 class="md:hidden text-lg font-bold pb-2 text-gray-100"> Propose tech you would like to see on the radar </h2>
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
    <h2 class="md:inline-block hidden text-4xl font-bold"> Propose tech you would like to see on the radar </h2>
    <div class="about-info pb-6">
      <p class="text-sm py-2 text-gray-300 font-light">The acronym zk-SNARK stands for "Zera-Knowledge Succinet
        Non-Interactive Argument of
        Knowledge," and refers to a proot construction where ane can prave passesaion of certain
        information, e.g. a secret key, without revealing that information, and without any interaction
        between the praver and verifier.
      </p>
    </div>
    <div class="proposition-form pb-6 w-full">
      <form action="" class="w-96 md:mx-auto">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required type="text" placeholder="Project or technology name">
        <select class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required name="category" id="category" placeholder="Category">
          <option class="bg-mvp-gray-dark" value="tools">Tools</option>
          <option class="bg-mvp-gray-dark" value="platforms">Platforms</option>
          <option class="bg-mvp-gray-dark" value="method-pat">Methods & Patterns</option>
          <option class="bg-mvp-gray-dark" value="lang-frm">Languages & Frameworks</option>
        </select>
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" required type="url" placeholder="Official project website or repository">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" type="text" placeholder="Project twitter account (optional)">
        <input class="w-full bg-transparent border-b-4 border-b-gray-300 pl-0 p-1 my-2" type="text" placeholder="Your twitter account if you want shout out (optional)">
        <button
            class="flex align-middle justify-center items-center mt-4 px-10 py-1 button filter-button-active rounded-full mb-2">
          <span class="leading-6 text-base font-bold"> Submit proposal </span>
        </button>
      </form>
    </div>
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
      newSubmit: {
        title: "",
        category: "",
        site: "",
        projectTwitter: "",
        personalTwitter: "",

      }

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

