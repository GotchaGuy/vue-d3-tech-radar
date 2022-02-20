<template>
  <section>
    <div class="grid grid-cols-4 container mx-auto w-6/7 2xl:w-4/5">
      <div v-for="(ring, i) in rings" class="col-span-1 mx-1" :key="i">
        <div class="cursor-pointer p-2 bg-mvp-gray-light text-center w-full" :id="'ring-' + i"
             @click="toggleRing(ring, i)">
          <h3 class="text-base font-bold capitalize">{{ ring.name }}</h3>
        </div>
        <ul class="ring-list">
          <li v-for="(ringItem, j) in getRingEntries(entries, i)"
              :class="(!ringItem.active) ? 'opacity-40' : ''"
              class="cursor-pointer ring-item p-2 my-0.5 bg-gray-800 bg-opacity-40 text-base font-light text-white hover:bg-mvp-gray-darker rounded-md"
              :key="j">

            <!--                class="radarData.quadrants[ringItem[j].quadrant].color"-->
            <div class="flex align-middle" @click="toggleSingleItem(ringItem, i, j); toggleDropDown(i, j)">
              <div class="inline-block category-color rounded-full p-2 mx-2 my-auto h-2 bg-mvp-green"></div>
              <span class="font-bold"> {{ ringItem.label }} </span>
            </div>

            <div v-if="showByIndex[i] === j" class="sub-info flex flex-col justify-start align-top pt-3 transition ease-in duration-200">
              <div class="block flex align-middle justify-items-start items-center px-2 mr-2 rounded-full">
                <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
                <span class="leading-6 text-xs font-normal"> Trial stage </span>
              </div>
              <div
                  class="flex align-middle justify-items-start items-center px-2 mr-2 rounded-full">
                <svg class="inline-block mr-2" xmlns="http://www.w3.org/2000/svg" width="21" height="21"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
                <span class="leading-6 text-xs font-normal"> New item </span>
              </div>
              <div class="flex align-middle justify-items-start items-center px-2 mr-2 rounded-full">
                <div class="category-color rounded-full bg-mvp-green h-2 px-3 py-2 mr-2"></div>
                <span class="leading-6 text-xs font-normal"> Tools </span>
              </div>
              <div
                  class="flex align-middle justify-items-start items-center px-2 mt-3 mr-2 rounded-md text-gray-300 hover:text-gray-100 hover:bg-mvp-gray-light"
                  @click="toggleModal(ringItem)">
                <span class="leading-6 text-xs font-normal pr-1"> Learn more </span>
                <svg style="width: 10px; height: 10px;" stroke="currentColor" viewBox="0 -3 24 24"
                     xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd" clip-rule="evenodd">
                  <path d="M21.883 12l-7.527 6.235.644.765 9-7.521-9-7.479-.645.764 7.529 6.236h-21.884v1h21.883z"/>
                </svg>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>

</template>

<script>

export default {
  name: "Grid",
  components: {},
  props: {
    radarData: Object
  },
  data() {
    return {
      modalDisplay: false,
      category: "",
      currentItem: {
        i: "",
        j: ""
      },
      previousItem: {
        i: "",
        j: ""
      },
      ringStatus: {
        currentI: "",
        previousI: "",
      },
      entries: [],
      rings: [],
      quadrants: [],
      showByIndex: [-1,-1,-1,-1],
    }
  },
  mounted() {
    // this.entries = this.radarData.entries;
    // this.rings = this.radarData.rings;
    this.emitter.on("data-to-grid-comp", (data) => {
      console.log(data.category);
      this.category = data.category;
      this.entries = data.radarData.entries;
      this.rings = data.radarData.rings;
      this.quadrants = data.radarData.quadrants;
    });

    this.checkCategory();
  },
  unmounted() {
    this.category = '';
  },
  methods: {
    getRingEntries(entries, ring) {
      var ringEntries = [];
      for (let k = 0; k < entries.length; k++) {
        if (entries[k].ring === ring) {
          ringEntries.push(entries[k]);
        }
      }
      return ringEntries;
    },
    toggleModal(item) {

      // this.toggleSingleItem(item, i, j);

      this.emitter.emit("toggle-modal", {
        displayed: !this.modalDisplay,
        item: item
      });

    },
    toggleSingleItem(item, i, j) {
      // when we connect the frontend to the db, add an if that will close modal if click on same item, load diff data on modal if click on diff item
      this.currentItem.i = i;
      this.currentItem.j = j;

      // console.log(this.currentItem.i + " ," + this.currentItem.j);
      // if (this.currentItem.j === this.previousItem.j && this.currentItem.i === this.previousItem.i || this.modalDisplay === false) {
      //   this.modalDisplay = !this.modalDisplay;
      //   this.toggleModal(item);
      // }
      if (this.currentItem.j === this.previousItem.j && this.currentItem.i === this.previousItem.i && this.modalDisplay === true) {
        this.modalDisplay = false;
        this.toggleModal(item);
      }

      for (let k = 0; k < this.entries.length; k++) {
        // instead of .label it will be .id when we connect to db
        if (this.entries[k].label !== item.label) {
          if (item.active === false) {
            item.active = true;
            this.entries[k].active = false;
          } else {
            if (this.currentItem.j === this.previousItem.j && this.currentItem.i === this.previousItem.i) {
              this.entries[k].active = !this.entries[k].active;
            } else {
              this.entries[k].active = false;
            }
          }
        }
      }

      // bugs currently
      // for (let k = 0; k < this.radarData.rings.length; k++) {
      //   if (this.radarData.rings[k] !== i) {
      //     console.log('ring-' + [k], i);
      //     document.getElementById('ring-' + [k]).classList.add("opacity-60");
      //   } else {
      //     document.getElementById('ring-' + [i]).classList.remove("opacity-60");
      //     document.getElementById('ring-' + [k]).classList.toggle("opacity-60");
      //   }
      // }

      this.previousItem = {
        i: i,
        j: j
      }
    },
    toggleRing(ring, i) {
      this.ringStatus.currentI = i;
      for (let k = 0; k < this.entries.length; k++) {
        if (this.ringStatus.currentI === this.ringStatus.previousI) {
          if (this.entries[k].ring !== ring.id) {
            this.entries[k].active = !this.entries[k].active;
          } else {
            this.entries[k].active = true;
          }
        } else {
          if (this.entries[k].ring !== ring.id) {
            this.entries[k].active = false;
          } else {
            this.entries[k].active = true;
          }
        }

      }
      this.ringStatus.previousI = i;
    },
    toggleDropDown(i, j) {
      this.showByIndex = [-1,-1,-1,-1];
      if (this.showByIndex[i] !== j) {
      this.showByIndex[i] = j;
      } else {
        this.showByIndex[i] = -1;
      }
    },
    checkCategory() {
      if (this.category === '') {
                    this.entries = this.radarData.entries;
                    this.rings = this.radarData.rings;
            } else {
        for (let i = 0; i < this.quadrants.length; i++) {
          if (this.quadrants[i].name === this.category) {
            this.entries = this.entries.filter(this.filterCat(this.entries, i));
          }
        }
      }
    },
    filterCat(entry, i) {
      return entry.quadrant = i;
    },
  }

}


</script>

