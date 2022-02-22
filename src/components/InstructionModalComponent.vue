<template>
  <section v-if="displayed"
           class="sidebar-modal-component h-screen sm:w-full lg:w-2/5 overflow-auto fixed bottom-0 z-5">
    <div class="lg:hidden p-6 bg-gray-200 opacity-40 h-32"></div>
    <div class="p-6 bg-mvp-gray-darker h-full">
      <div class="flex justify-between items-start">
        <h3 class="lg:inline-block hidden text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB3</span> Technology radar </h3>
        <h2 class="lg:hidden text-lg font-bold pb-2 text-gray-100"> What is Web3 tech radar and how to read it?  </h2>
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
      <h2 class="lg:inline-block hidden text-4xl font-bold"> What is Web3 tech radar and how to read it? </h2>
      <div class="about-info pb-6">

      </div>
      <ul class="info-accordion pb-6 p-2">
        <li class="info-item-container rounded-sm my-1 " v-for="(infoItem, i) in infoList" :key="i"
            @click="infoItem.active = !infoItem.active" :class="(infoItem.active) ? 'bg-mvp-gray-light' : ''">
          <div class="flex justify-between p-2 rounded-sm cursor-pointer group hover:bg-mvp-gray-light">
            <span class="category-item w-full text-md font-normal"> {{ infoItem.title }}</span>
            <div
                class="rounded-full text-mvp-purple group-hover:text-purple-500 flex align-middle justify-center items-center"
                :class="(infoItem.active) ? 'transform rotate-180' : ''">
              <svg class="x-button-icon inline-block" style="width: 16px; height: 16px;"
                   xmlns="http://www.w3.org/2000/svg"
                   fill-rule="evenodd" clip-rule="evenodd" stroke="currentColor" viewBox="0 0 24 24"
                   preserveAspectRatio="xMidYMin meet">
                <path d="M23.245 4l-11.245 14.374-11.219-14.374-.781.619 12 15.381 12-15.391-.755-.609z"/>
              </svg>
            </div>
          </div>
          <div v-if="infoItem.active" class="p-2">
            <p v-for="(paragraph, j) in infoItem.paragraphs" :key="j" class="text-sm pb-2 text-gray-300 font-light">
              {{ paragraph }} </p>
          </div>
        </li>

      </ul>
      <button
          class="flex align-middle justify-center items-center mt-4 px-10 py-1 button filter-button-active rounded-full mb-2">
        <span class="leading-6 text-base font-bold"> I'm ready to explore </span>
      </button>
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
      infoList: [
        {
          title: "What is the tech radar?",
          active: false,
          paragraphs: ["", ""]
        },
        {
          title: "How to read it?",
          active: false,
          paragraphs: ["", ""]
        },
        {
          title: "Quadrants",
          active: false,
          paragraphs: ["", ""]
        },
        {
          title: "Rings",
          active: false,
          paragraphs: [
            "Adopt ring represents blips that we think you should seriously consider using. We don't say that you should use these for every project; any tool should onlų be used in an appropriate context. However we do think that a blip in the Adopt ring represents something where there's no doubt that it's proven and mature for use.",
            "Trial ring is for blips that we think are ready for use, but not as completelu proven as those in the Adopt ring. So for mast organizations we think you should use these on a trial basis, to decide whether they should be part of your toolkit. Typically we've used trial blips in production, but we realize that readers are more cautious than us.",
            "Assess ring are things to look at closely, but not necessarily trial yet - unless you think they would be a particularly good fit for you. Typically, blips in the Assess ring are things that we think are interesting and worth keeping an eye on",
            "Hold ring is for things that, even though they are accepted in the industry, we haven't had a good experience with. Therefore we are calling them out to warn you that you may run into trouble with them as well. Sometimes it means we think they're irredeemably flawed; or just being misused. We do place things in the Hold ring that we wish the industry wouldn't use."
          ]
        },
        {
          title: "Who created Web3 Tech radar?",
          active: false,
          paragraphs: ["", ""]
        },
      ],

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

