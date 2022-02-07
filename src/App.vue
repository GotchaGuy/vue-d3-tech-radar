<template>
  <div class="section grid grid-cols-10">

    <div class="col-span-4 p-5 flex flex-col justify-between">
      <div>
        <h2 class="text-4xl font-light py-2"><span class="font-bold">WEB 3</span> Technology radar</h2>
        <p class="w-96 inline-block text-sm font-light pb-5"> Lorem ipsum dolor sit amet, consectetur adipiscing elit.
          Nam a congue elit. Maecenas ultrices lectus et eros mollis eleifend. Sed a nibh felis. Sed pulvinar, enim vel
          elementum vehicula, metus nulla commodo erat, quis posuere diam augue non nisl. </p>
        <div class="display-type-container">
          <div class="w-96 display-type-inner rounded-full inline-block">
            <button class="align-middle w-1/3 button filter-button rounded-full filter-button-active">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base"> Radar </span>
            </button>
            <button class="align-middle w-1/3 button filter-button rounded-full">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base"> Grid </span>
            </button>
            <button class="align-middle w-1/3 button filter-button rounded-full">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base"> Quadrant </span>
            </button>
          </div>
        </div>
      </div>
      <div>

        <h3>Categories</h3>
        <div class="icon"></div>
        <ul class="category-list">
          <li class="category-item-container">
            <span class="category-item">Tools</span>
            <div class="category-color"></div>
          </li>
        </ul>
      </div>
    </div>
    <div class="col-span-6 p-5">


    </div>
  </div>
</template>

<script>

// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  }
}
</script>

<style>
/*#app {*/
/*  font-family: Avenir, Helvetica, Arial, sans-serif;*/
/*  -webkit-font-smoothing: antialiased;*/
/*  -moz-osx-font-smoothing: grayscale;*/
/*  text-align: center;*/
/*  color: #2c3e50;*/
/*  !*margin-top: 60px;*!*/
/*}*/
</style>
