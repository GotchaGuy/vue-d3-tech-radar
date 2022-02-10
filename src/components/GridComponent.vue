<template>
  <section>
    <div class="grid grid-cols-4 container mx-auto w-4/5">
      <div v-for="(ring, i) in radarData.rings" class="col-span-1 mx-1"
           :key="i">
        <div class="p-2 bg-mvp-gray-light text-center w-full">
          <h3 class="text-base font-bold capitalize">{{ ring.name }}</h3>
        </div>
        <ul class="ring-list">
          <li v-for="(ringItem, j) in getRingEntries(entries, i)" @click="toggleModal(ringItem, i, j)"
              :class="(!ringItem.active) ? 'opacity-60' : ''"
              class="cursor-pointer ring-item p-2 my-0.5 bg-gray-800 bg-opacity-40 text-base font-light text-white hover:bg-mvp-gray-darker rounded-md flex align-middle"
              :key="j">

            <!--                class="radarData.quadrants[ringItem[j].quadrant].color"-->
            <div class="inline-block category-color rounded-full p-2 mx-2 my-auto h-2 bg-mvp-green"></div>
            <span> {{ ringItem.label }} </span>
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
      currentItem: {
        i: "",
        j: ""
      },
      previousItem: {
        i: "",
        j: ""
      },
      entries: [],
    }
  },
  mounted() {
    this.entries = this.radarData.entries
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
    toggleModal(item, i, j) {
      // when we connect the frontend to the db, add an if that will close modal if click on same item, load diff data on modal if click on diff item
      this.currentItem.i = i;
      this.currentItem.j = j;
      // console.log(this.currentItem.i + " ," + this.currentItem.j);
      if (this.currentItem.j === this.previousItem.j && this.currentItem.i === this.previousItem.i || this.modalDisplay === false) {
        this.modalDisplay = !this.modalDisplay;
      }
      this.activateSingleItem(item, this.currentItem, this.previousItem);
      this.emitter.emit("toggle-modal", {
        displayed: this.modalDisplay,
        item: item
      });
      this.previousItem = {
        i: i,
        j: j
      }
    },
    activateSingleItem(item, current, previous) {
      for (let k = 0; k < this.entries.length; k++) {
         // instead of .label it will be .id when we connect to db
        if (this.entries[k].label !== item.label) {
          if (item.active === false) {
            item.active = true;
            this.entries[k].active = false;
          } else {
            if (current.j === previous.j && current.i === previous.i) {
            this.entries[k].active = !this.entries[k].active;
            } else {
              this.entries[k].active = false;
            }
          }
        }
      }
    }
  },

}
</script>

