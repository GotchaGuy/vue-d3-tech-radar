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
    <h2 class="text-4xl font-bold"> My tech list </h2>
    <div class="about-info pb-6">
      <p class="text-sm py-2 text-gray-300 font-light">
        This tech list is saved in the local storage of your device. You can remove it any time you want.
        Also you can always export your ist as CSV fle.
      </p>
    </div>
    <div class="tech-list pb-6">
      <div class="tech-item bg-mvp-gray-light my-2 p-3 cursor-pointer hover:bg-gray-800" style="border-radius: 15px">
        <h3 class="text-2xl font-bold pl-2">zk-SNARKs</h3>
        <div class="flex justify-start">
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> Trial stage </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> New item </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
            <span class="leading-6 text-base font-bold"> Tools </span>
          </div>
        </div>
      </div>

      <div class="tech-item bg-mvp-gray-light my-2 p-3 cursor-pointer hover:bg-gray-800" style="border-radius: 15px">
        <h3 class="text-2xl font-bold pl-2">zk-SNARKs</h3>
        <div class="flex justify-start">
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> Trial stage </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> New item </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
            <span class="leading-6 text-base font-bold"> Tools </span>
          </div>
        </div>
      </div>

      <div class="tech-item bg-mvp-gray-light my-2 p-3 cursor-pointer hover:bg-gray-800" style="border-radius: 15px">
        <h3 class="text-2xl font-bold pl-2">zk-SNARKs</h3>
        <div class="flex justify-start">
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> Trial stage </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                 viewBox="0 0 24 24">
              <path
                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
            </svg>
            <span class="leading-6 text-base font-bold"> New item </span>
          </div>
          <div class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
            <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
            <span class="leading-6 text-base font-bold"> Tools </span>
          </div>
        </div>
      </div>

    </div>
  </section>

</template>


<script>

export default {
  name: "TechListModal",
  components: {},
  props: {},
  data() {
    return {
      displayed: false,

    }
  },
  mounted() {
    this.emitter.on("toggle-tech-list-modal", (data) => {
      this.displayed = data.displayed;
    });
  },
  methods: {},

}
</script>



