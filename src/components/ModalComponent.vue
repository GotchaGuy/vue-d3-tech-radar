<template>
  <section v-if="displayed" class="modal-component p-6 fixed bg-mvp-gray-darker w-2/5">
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
    <h2 class="text-5xl font-bold"> zk-SNARKs</h2>
    <div class="flex justify-start py-3">
      <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-light">
        <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
          <path
              d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
        </svg>
        <span class="leading-6 text-base font-bold"> Trial stage </span>
      </div>
      <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-light">
        <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
          <path
              d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
        </svg>
        <span class="leading-6 text-base font-bold"> New item </span>
      </div>
      <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-light">
        <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
        <span class="leading-6 text-base font-bold"> Tools </span>
      </div>
    </div>
    <div class="about-info pb-6">
      <h3 class="text-lg pb-2 text-white font-bold"> What is it about? </h3>
      <p class="text-sm py-2 text-gray-300 font-light">The acronym zk-SNARK stands for "Zera-Knowledge Succinet
        Non-Interactive Argument of
        Knowledge," and refers to a proot construction where ane can prave passesaion of certain
        information, e.g. a secret key, without revealing that information, and without any interaction
        between the praver and verifier.
      </p>
      <p class="text-sm py-2 text-gray-300 font-light">
        Rather than recording al the data from a business tranaaction or process, zk-SNARKS allow
        businesses to store only the praof of the transaction an a node. Companies can koep their
        seraitive data to themselves, while still maintaining conticence in a connected record af
        provena. to stare only the proof of the transaction on a nade. Dompanies can kaep their
        sensitive data to themselves, while still maintaining conticence in a connected record of
        provenance.</p>
      <p class="text-sm py-2 text-gray-300 font-light">Learn more at: <a href="https//2.cash/technology/zkanarks/">https//2.cash/technology/zkanarks/</a>
      </p>
    </div>
    <div class="experience-info pb-6">
      <h3 class="text-lg pb-2 text-white font-bold"> Our experience </h3>
      <p class="text-sm py-2 text-gray-300 font-light">The acronym zk-SNARK stands for "Zera-Knowledge Succinet
        Non-Interactive Argument of
        Knowledge," and refers to a proot construction where ane can prave passesaion of certain
        information, e.g. a secret key, without revealing that information, and without any interaction
        between the praver and verifier.
      </p>
    </div>
    <div class="projects-info pb-6">
      <h3 class="text-lg pb-2 text-white font-bold"> Notable projects </h3>
      <div class="project-list">
        <button
            class="flex align-middle justify-center items-center py-1 px-2 mr-2 button filter-button rounded-full border-2 border-transparent hover:border-white">
          <span class="leading-6 text-base font-bold"> Hina </span>
        </button>
        <button
            class="flex align-middle justify-center items-center py-1 px-2 mr-2 button filter-button rounded-full  border-2 border-transparent hover:border-white">
          <span class="leading-6 text-base font-bold"> Zokrates </span>
        </button>
        <button
            class="flex align-middle justify-center items-center py-1 px-2 mr-2 button filter-button rounded-full  border-2 border-transparent hover:border-white">
          <span class="leading-6 text-base font-bold"> Gnark </span>
        </button>
        <button
            class="flex align-middle justify-center items-center py-1 px-2 mr-2 button filter-button rounded-full  border-2 border-transparent hover:border-white">
          <span class="leading-6 text-base font-bold"> Pysnork </span>
        </button>
      </div>
    </div>
    <button class="flex align-middle justify-center items-center py-1 px-2 button filter-button filter-button-active rounded-full mb-2">
      <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
          <path
              d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
        </svg>
      <span class="leading-6 text-base font-bold"> Save to my tech list </span>
    </button>
  </section>

</template>


<script>

export default {
  name: "Modal",
  components: {},
  props: {},
  data() {
    return {
      displayed: false,
      item: {}

    }
  },
  mounted() {
    this.emitter.on("toggle-modal", modalDisplay => {
      this.displayed = modalDisplay;
    }, item => {
      this.item = item;
    });
  },
  methods: {
    methodHere() {
    },
  },

}
</script>

<style>
section.modal-component {
  height: 100vh;
}

</style>

