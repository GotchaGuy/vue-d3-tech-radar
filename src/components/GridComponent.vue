<template>
  <section>
    <h2>Grid</h2>
    <p>{{this.radarData.entries[0].label}}</p>
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
      sumData: ""
    }
  },
  mounted() {
    console.log(this.radarData);
  },
  methods: {
    methodhere() {

    },
  },

}
</script>

