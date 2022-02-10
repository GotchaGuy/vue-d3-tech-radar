<template>
  <section>
    <div class="grid grid-cols-4 container mx-auto w-4/5">
      <div v-for="(ring, i) in radarData.rings" class="col-span-1 mx-1"
           :key="i">
        <div class="p-2 bg-mvp-gray-light text-center w-full">
          <h3 class="text-base font-bold capitalize">{{ ring.name }}</h3>
        </div>
        <ul class="ring-list">
          <li v-for="(ringItem, j) in getRingEntries(radarData.entries, i)" @click="toggleModal(ringItem, i, j)"
              class="ring-item p-2 my-0.5 bg-gray-800 bg-opacity-40 text-base font-light text-white hover:bg-mvp-gray-darker rounded-md flex align-middle" :key="j">
<!--            <svg class="inline-block mx-2 opacity-100" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">-->
<!--              <path-->
<!--                  d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>-->
<!--            </svg>-->

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
    }
  },
  mounted() {
    // console.log(this.radarData);
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
      console.log(this.currentItem.i + " ," + this.currentItem.j);
      if (this.currentItem.j === this.previousItem.j && this.currentItem.i === this.previousItem.i || this.modalDisplay === false) {
      this.modalDisplay = !this.modalDisplay;
      }
      this.emitter.emit("toggle-modal", {
        displayed:this.modalDisplay,
        item: item
      });
      this.previousItem = {
        i: i,
        j: j
      }

    },
  },

}
</script>

