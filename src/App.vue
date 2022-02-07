<template>
  <div class="main-section grid grid-cols-10">
<!--    left section-->
    <section class="col-span-4 p-5 flex flex-col justify-between">
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
              <span class="leading-6 text-base font-bold"> Radar </span>
            </button>
            <button class="align-middle w-1/3 button filter-button rounded-full">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Grid </span>
            </button>
            <button class="align-middle w-1/3 button filter-button rounded-full">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Quadrant </span>
            </button>
          </div>
        </div>
      </div>
      <div class="w-1/3">
        <section class="categories">
          <div class="flex justify-between pb-2">
            <h3 class="text-base font-bold inline-block">Categories</h3>
            <div class="icon text-base font-bold inline-block px-2">?</div>
          </div>
          <ul class="category-list pb-4">
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">Tools</span>
              <div class="category-color rounded-full bg-mvp-green px-3 my-1"></div>
            </li>
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">Platforms</span>
              <div class="category-color rounded-full bg-mvp-blue px-3 my-1"></div>
            </li>
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">Methods & Patterns</span>
              <div class="category-color rounded-full bg-mvp-orange px-3 my-1"></div>
            </li>
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">Languages & Frameworks</span>
              <div class="category-color rounded-full bg-mvp-purple px-3 my-1"></div>
            </li>
          </ul>
        </section>
        <section class="statuses">
          <div class="flex justify-between pb-2">
            <h3 class="text-base font-bold inline-block">Statuses</h3>
            <div class="icon text-base font-bold inline-block px-2">?</div>
          </div>
          <ul class="category-list pb-4">
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">Tools</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block text-white" xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">Platforms</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block text-white" xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">Methods & Patterns</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                  <path color="white"
                        d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">Languages & Frameworks</span>
              <div class="category-color rounded-full pr-1 text-white">
                <svg class="inline-block text-white" xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
          </ul>
        </section>
        <div class="user-buttons-container">
          <button class="align-middle w-full button filter-button rounded-full mb-2">
            <span class="leading-6 text-base font-bold"> How to read this radar? </span>
          </button>
          <button class="align-middle w-full button filter-button rounded-full mb-2">
            <span class="leading-6 text-base font-bold"> Propose new tech! </span>
          </button>
          <button class="align-middle w-full button filter-button filter-button-active rounded-full mb-2">
            <span class="leading-6 text-base font-bold"> My tech list (3) </span>
          </button>
        </div>
      </div>
    </section>
<!--    right section-->
    <section class="col-span-6 p-5">


    </section>
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
