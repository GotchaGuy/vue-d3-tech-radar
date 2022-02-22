<template>
  <section v-if="displayed"
           class="sidebar-modal-component h-screen sm:w-full md:w-2/5 bg-mvp-gray-darker overflow-auto fixed bottom-0">
    <div class="md:hidden p-6 bg-gray-200 opacity-40 h-32"></div>
    <div class="p-6 bg-mvp-gray-darker h-full">
      <div class="flex justify-between items-start">
        <h3 class="md:inline-block hidden text-lg font-light pb-2 text-gray-300"><span class="font-bold">WEB3</span>
          Technology radar </h3>
        <h2 class="md:hidden text-lg font-bold pb-2 text-gray-100"> My tech list </h2>
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
      <h2 class="md:inline-block hidden text-4xl font-bold"> My tech list </h2>
      <div class="about-info pb-6">
        <p class="text-sm py-2 text-gray-300 font-light">
          This tech list is saved in the local storage of your device. You can remove it any time you want.
          Also you can always export your ist as CSV fle.
        </p>
      </div>
      <div class="tech-list pb-6">
        <div v-for="(blip, i) in cachedList" :key="i" @click="toggleActive(blip, i)"
             :class="(!blip.active) ? 'opacity-40' : ''"
             class="group tech-item bg-mvp-gray-dark my-2 p-3 cursor-pointer hover:bg-mvp-gray-light"
             style="border-radius: 15px">
          <div class="flex justify-between pl-2">
            <h3 class="text-2xl font-bold inline-block"> {{ blip.label }} </h3>
            <!--            invisible group-hover:visible-->
            <div class="relative">
              <div
                  class="hidden text-xs bg-black text-white bg-opacity-80 p-1 absolute -top-7 -left-20 rounded shadow-xl w-32"
                  :id="'tooltip-' + i">
                Remove from list
              </div>
              <button class="text-gray-300" :id="'bookmark-' + i" @mouseenter="toggleTooltip(i)"
                      @mouseleave="toggleTooltip(i)" @click="removeBlip(i)">
                <svg class="inline-block text-white hover:text-gray-200" width="24" height="24"
                     xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd"
                     clip-rule="evenodd" preserveAspectRatio="none" viewBox="0 0 24 24">
                  <path class="" fill="currentColor" stroke="currentColor" d="M18 24l-6-5.269-6 5.269v-24h12v24z"/>
                </svg>
              </button>
            </div>
          </div>
          <div class="flex justify-start">
            <div
                class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
              <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                   viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Trial stage </span>
            </div>
            <div
                class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
              <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                   viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> New item </span>
            </div>
            <div
                class="flex align-middle justify-center items-center py-1 px-2 mr-2 rounded-full hover:bg-mvp-gray-dark">
              <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
              <span class="leading-6 text-base font-bold"> Tools </span>
            </div>
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
      cachedList: [],
      hardCodedList: [
        {
          "quadrant": 3,
          "ring": 2,
          "label": "Item with long name",
          "active": true,
          "moved": 0
        },
        {
          "quadrant": 3,
          "ring": 3,
          "label": "AWS Data Pipeline",
          "active": true,
          "moved": 0
        },
        {
          "quadrant": 3,
          "ring": 0,
          "label": "AWS EMR",
          "active": true,
          "moved": 0
        },
      ],
    }
  },
  mounted() {
    this.updateList();
    // console.log(this.cachedList);

    this.emitter.on("toggle-tech-list-modal", (data) => {
      this.displayed = data.displayed;
    });
    this.emitter.on("update-cached-list", () => {
      this.updateList();
    });
  },
  methods: {
    toggleActive(blip, i) {
      this.currentBlip = i;

      for (let k = 0; k < this.currentList.length; k++) {
        // instead of .label it will be .id when we connect to db
        if (this.currentList[k].label !== blip.label) {
          if (blip.active === false) {
            blip.active = true;
            // document.getElementById('blip-' + [k]).classList.remove("invisible");
            this.currentList[k].active = false;
          } else {
            if (this.currentBlip === this.previousBlip) {
              this.currentList[k].active = !this.currentList[k].active;
            } else {
              this.currentList[k].active = false;
            }
          }
        }
      }
      this.previousBlip = i;
    },
    toggleTooltip(i) {
      document.querySelector('#tooltip-' + i).classList.toggle("hidden");
    },
    removeBlip(i) {
      this.cachedList.splice(i, 1);
      this.saveCachedList();
    },
    saveCachedList() {
      const parsed = JSON.stringify(this.cachedList);
      localStorage.setItem('techList', parsed);
    },
    isSaved() {
      if (!this.cachedList) {
        return;
      }
      for (let i = 0; i < this.cachedList.length; i++) {
        if (this.cachedList[i].label === this.item.label) {
          this.saveable = false;
        }
      }
    },
    updateList() {
      if (localStorage.getItem('techList')) {
      try {
        this.cachedList = JSON.parse(localStorage.getItem('techList'));
        console.log(this.cachedList);
      } catch (e) {
        localStorage.removeItem('techList');
      }
    }
    }
  },

}
</script>



