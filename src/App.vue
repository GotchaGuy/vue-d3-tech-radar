<template>
  <div class="main-section grid grid-cols-10">
    <!--    left section-->
    <section class="col-span-10 md:col-span-4 p-6 flex flex-col justify-between relative">
      <div>
        <h2 class="text-4xl font-light pb-2"><span class="font-bold">WEB 3</span> Technology radar</h2>
        <p class="w-full md:w-96 inline-block text-sm font-light pb-5"> Lorem ipsum dolor sit amet, consectetur
          adipiscing elit.
          Nam a congue elit. Maecenas ultrices lectus et eros mollis eleifend. Sed a nibh felis. Sed pulvinar, enim vel
          elementum vehicula, metus nulla commodo erat, quis posuere diam augue non nisl. </p>
        <div class="md:inline-block hidden display-type-container">
          <div class="w-96 display-type-inner bg-mvp-gray-light rounded-full inline-block">
            <button @click="openTab = 'Radar'" :class="{'filter-button-active': openTab === 'Radar'}"
                    class="flex align-middle justify-center items-center py-1 px-2 w-1/3 button filter-button rounded-full border-2 border-transparent hover:border-white">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Radar </span>
            </button>
            <button @click="openTab = 'Grid'" :class="{'filter-button-active': openTab === 'Grid'}"
                    class="flex align-middle justify-center items-center py-1 px-2 w-1/3 button filter-button rounded-full  border-2 border-transparent hover:border-white">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Grid </span>
            </button>
            <button @click="openTab = 'Quadrant'" :class="{'filter-button-active': openTab === 'Quadrant'}"
                    class="flex align-middle justify-center items-center py-1 px-2 w-1/3 button filter-button rounded-full  border-2 border-transparent hover:border-white">
              <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 24 24">
                <path
                    d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
              </svg>
              <span class="leading-6 text-base font-bold"> Quadrant </span>
            </button>
          </div>
        </div>
      </div>
      <div class="w-full lg:w-4/5 xl:w-3/5 2xl:w-2/5 mb-5">
        <section class="md:hidden categories-mobile grid gap-2 grid-cols-2 w-full mb-5">
          <button @click="openTab = ''" :class="{'': openTab === ''}"
                  class="overflow-hidden relative p-2 basis-1/2 h-24 bg-mvp-gray-darker button rounded-lg border-2 border-transparent hover:border-white">
            <span class="absolute bottom-3 left-3 leading-6 text-base font-bold"> Tools </span>
            <svg class="absolute bottom-0 right-0 " height="50" width="50">
              <circle class="text-mvp-green opacity-40" cx="50" cy="50" r="50" fill="currentColor"/>
              <circle class="text-mvp-green opacity-60" cx="50" cy="50" r="40" fill="currentColor"/>
              <circle class="text-mvp-green opacity-80" cx="50" cy="50" r="30" fill="currentColor"/>
              <circle class="text-mvp-green" cx="50" cy="50" r="20" fill="currentColor"/>
              Sorry, your browser does not support inline SVG.
            </svg>
          </button>
          <button @click="openTab = ''" :class="{'': openTab === ''}"
                  class="overflow-hidden relative p-2 basis-1/2 h-24 bg-mvp-gray-darker button rounded-lg border-2 border-transparent hover:border-white">
            <svg class="absolute bottom-0 left-0 " height="50" width="50">
              <circle class="text-mvp-blue opacity-40" cx="0" cy="50" r="50" fill="currentColor"/>
              <circle class="text-mvp-blue opacity-60" cx="0" cy="50" r="40" fill="currentColor"/>
              <circle class="text-mvp-blue opacity-80" cx="0" cy="50" r="30" fill="currentColor"/>
              <circle class="text-mvp-blue" cx="0" cy="50" r="20" fill="currentColor"/>
              Sorry, your browser does not support inline SVG.
            </svg>
            <span class="absolute bottom-3 right-3 leading-6 text-base font-bold"> Platforms </span>
          </button>
          <button @click="openTab = ''" :class="{'': openTab === ''}"
                  class="overflow-hidden relative p-2 basis-1/2 h-24 bg-mvp-gray-darker button rounded-lg border-2 border-transparent hover:border-white">
            <span class="absolute bottom-3 left-3 text-left leading-6 text-base font-bold w-32"> Methods & Patterns </span>
            <svg class="absolute top-0 right-0 " height="50" width="50">
              <circle class="text-mvp-orange opacity-40" cx="50" cy="0" r="50" fill="currentColor"/>
              <circle class="text-mvp-orange opacity-60" cx="50" cy="0" r="40" fill="currentColor"/>
              <circle class="text-mvp-orange opacity-80" cx="50" cy="0" r="30" fill="currentColor"/>
              <circle class="text-mvp-orange" cx="50" cy="0" r="20" fill="currentColor"/>
              Sorry, your browser does not support inline SVG.
            </svg>
          </button>
          <button @click="openTab = ''" :class="{'': openTab === ''}"
                  class="overflow-hidden relative p-2 basis-1/2 h-24 bg-mvp-gray-darker button rounded-lg border-2 border-transparent hover:border-white">
            <svg class="absolute top-0 left-0 " height="50" width="50">
              <circle class="text-mvp-purple opacity-40" cx="0" cy="0" r="50" fill="currentColor"/>
              <circle class="text-mvp-purple opacity-60" cx="0" cy="0" r="40" fill="currentColor"/>
              <circle class="text-mvp-purple opacity-80" cx="0" cy="0" r="30" fill="currentColor"/>
              <circle class="text-mvp-purple" cx="0" cy="0" r="20" fill="currentColor"/>
              Sorry, your browser does not support inline SVG.
            </svg>
            <span class="absolute bottom-3 right-3 text-right leading-6 text-base font-bold w-32"> Languages & Frameworks </span>
          </button>
        </section>
        <section class="md:inline-block hidden categories">
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
        <section class="md:inline-block hidden statuses">
          <div class="flex justify-between pb-2">
            <h3 class="text-base font-bold inline-block">Statuses</h3>
            <div class="icon text-base font-bold inline-block px-2">?</div>
          </div>
          <ul class="category-list pb-4">
            <li class="category-item-container flex justify-between pb-1">
              <span class="category-item w-full text-sm font-light">New or highlight</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block text-white" xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">Moved inside</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block text-white" xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                     viewBox="0 0 24 24">
                  <path
                      d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">Moved outside</span>
              <div class="category-color rounded-full pr-1">
                <svg class="inline-block" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                  <path color="white"
                        d="M12 3c-4.006 0-7.267 3.141-7.479 7.092-2.57.463-4.521 2.706-4.521 5.408 0 3.037 2.463 5.5 5.5 5.5h13c3.037 0 5.5-2.463 5.5-5.5 0-2.702-1.951-4.945-4.521-5.408-.212-3.951-3.473-7.092-7.479-7.092z"/>
                </svg>
              </div>
            </li>
            <li class="category-item-container flex justify-between">
              <span class="category-item w-full text-sm font-light">No change</span>
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
        <div class="user-buttons-container pb-10 md:pb-0">
          <button @click="toggleInstructionModal()"
                  class="flex align-middle justify-center items-center py-1 px-2 w-full button bg-mvp-gray-light filter-button rounded-full mb-2 border-2 border-transparent hover:border-white">
            <span class="leading-6 text-base font-bold"> How to read this radar? </span>
          </button>
          <button @click="togglePropositionFormModal()"
                  class="flex align-middle justify-center items-center py-1 px-2 w-full button bg-mvp-gray-light filter-button rounded-full mb-2 border-2 border-transparent hover:border-white">
            <span class="leading-6 text-base font-bold"> Propose new tech! </span>
          </button>
          <button @click="toggleTechListModal()"
                  class="flex align-middle justify-center items-center py-1 px-2 w-full button bg-mvp-gray-light filter-button filter-button-active rounded-full mb-2">
            <span class="leading-6 text-base font-bold"> My tech list (3) </span>
          </button>
        </div>
      </div>

      <!--      made with <3-->
      <div class="bg-gray-700 p-3 rounded-lg text-center md:text-right inline-block md:fixed md:bottom-8 md:right-8">
        <h3 class="text-base font-bold">Made with <span class="text-red-500">&hearts;</span> by 3327</h3>
        <span class="text-sm font-bold text-gray-500">Web 3 tech vanguards</span>
      </div>

    </section>

    <!--    right section-->
    <section class="md:inline-block hidden col-span-6 p-6">
      <div :class="{'hidden': openTab !== 'Radar', 'block': openTab === 'Radar'}">
        <Radar :radarData="radarVisualization"/>
      </div>
      <div :class="{'hidden': openTab !== 'Grid', 'block': openTab === 'Grid'}">
        <Grid
            :radarData="radarVisualization"
        />
      </div>
      <div :class="{'hidden': openTab !== 'Quadrant', 'block': openTab === 'Quadrant'}">
        <Quadrant/>
      </div>
    </section>

    <Modal/>
    <PropositionFormModal/>
    <TechListModal/>
    <InstructionModal/>
  </div>
</template>

<script>
import Radar from './components/RadarComponent.vue'
import Grid from './components/GridComponent.vue'
import Quadrant from './components/QuadrantComponent.vue'
import Modal from './components/ModalComponent.vue'
import PropositionFormModal from './components/PropositionFormModalComponent.vue'
import TechListModal from './components/TechListModalComponent.vue'
import InstructionModal from './components/InstructionModalComponent.vue'

export default {
  name: 'App',
  components: {
    Radar,
    Grid,
    Quadrant,
    Modal,
    PropositionFormModal,
    TechListModal,
    InstructionModal,

  }, data() {
    return {
      buttonsArr: [{}, {}, {}, {}],
      modalDisplay: false,
      propFormDisplay: false,
      techListDisplay: false,
      instructionDisplay: false,
      openTab: "Grid",
      currentItemId: "",
      radarVisualization: {
        svg_id: "radar",
        width: 1450,
        height: 1000,
        colors: {
          background: "#242429",
          grid: "#bbb",
          inactive: "#ddd",
          text: "#fff"
        },
        title: "WEB3 Technology Radar",
        quadrants: [
          {name: "Tools", color: "#8aedb1", tw: "mvp-green"},
          {name: "Platforms", color: "#d8fefe", tw: "mvp-blue"},
          {name: "Methods & patterns", color: "#ffc895", tw: "mvp-orange"},
          {name: "Languages & Frameworks", color: "#db6af9", tw: "mvp-purple"},
        ],
        rings: [
          {name: "Adopt", id: 0},
          {name: "Trial", id: 1},
          {name: "Assess", id: 2},
          {name: "Hold", id: 3}
        ],
        print_layout: true,
        // zoomed_quadrant: 0,

        //ENTRIES
        entries: [
          {
            "quadrant": 3,
            "ring": 2,
            "label": "Item with long name",
            // "label": "AWS Athena",
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
          {
            "quadrant": 3,
            "ring": 2,
            "label": "AWS Glue",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 3,
          //   "ring": 0,
          //   "label": "Airflow",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 3,
          //   "ring": 0,
          //   "label": "Databricks",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 3,
            "ring": 1,
            "label": "Flink",
            "link": "",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 3,
            "ring": 1,
            "label": "Google BigQuery",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 3,
            "ring": 3,
            "label": "Hadoop",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 3,
            "ring": 1,
            "label": "Presto",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 3,
            "ring": 0,
            "label": "Spark",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 3,
            "ring": 3,
            "label": "YARN",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 2,
          //   "ring": 0,
          //   "label": "AWS test",
          //   "active": true,
          //   "moved": 1
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 0,
          //   "label": "AWS S3",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 2,
            "ring": 3,
            "label": "Aerospike",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 2,
            "ring": 1,
            "label": "Amazon Redshift",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 2,
            "ring": 0,
            "label": "Cassandra",
            "link": "",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "Consul",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "CouchBase",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 2,
            "ring": 2,
            "label": "Druid",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 2,
            "ring": 0,
            "label": "Elasticsearch",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 2,
            "ring": 0,
            "label": "Exasol",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 2,
            "ring": 2,
            "label": "Google Bigtable",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "HBase",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 2,
            "ring": 1,
            "label": "HDFS",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "Hazelcast",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "Memcached",
          //   "active": true,
          //   "moved": 1
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "MongoDB",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "MySQL",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 3,
          //   "label": "Oracle DB",
          //   "active": true,
          //   "moved": 1
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 0,
          //   "label": "PostgreSQL",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 2,
          //   "ring": 0,
          //   "label": "Redis",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 2,
            "ring": 2,
            "label": "RocksDB",
            "active": true,
            "moved": 1
          },
          {
            "quadrant": 2,
            "ring": 3,
            "label": "Solr",
            "active": true,
            "moved": 2
          },
          {
            "quadrant": 2,
            "ring": 3,
            "label": "ZooKeeper",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 2,
          //   "ring": 0,
          //   "label": "etcd",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "AWS CloudFormation",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "AWS CloudFront",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 1,
            "ring": 1,
            "label": "AWS Lambda",
            "active": true,
            "moved": 2
          },
          {
            "quadrant": 1,
            "ring": 0,
            "label": "Amazon SageMaker",
            "active": true,
            "moved": 1
          },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "Docker",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "Kubernetes",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "Nginx",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 1,
          //   "ring": 0,
          //   "label": "OpenTracing",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 1,
            "ring": 3,
            "label": "STUPS",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 1,
            "ring": 0,
            "label": "Skipper",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 1,
            "ring": 2,
            "label": "Slurm",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 1,
            "ring": 0,
            "label": "ZMON",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 3,
            "label": "Clojure",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 0,
            "label": "Go",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 0,
            "label": "GraphQL",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 3,
            "label": "Haskell",
            "link": "",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "Java",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "JavaScript",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "Kotlin",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "OpenAPI (Swagger)",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 0,
            "ring": 0,
            "label": "Python",
            "link": "",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 2,
            "label": "R",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 0,
            "ring": 3,
            "label": "Rust",
            "link": "",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "Scala",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "Swift",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 0,
          //   "ring": 0,
          //   "label": "TypeScript",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 3,
            "ring": 1,
            "label": "AWS Kinesis",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 3,
            "ring": 0,
            "label": "AWS SNS",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 3,
          //   "ring": 0,
          //   "label": "AWS SQS",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 3,
            "ring": 3,
            "label": "ActiveMQ",
            "active": true,
            "moved": 0
          },
          {
            "quadrant": 3,
            "ring": 3,
            "label": "HornetQ",
            "active": true,
            "moved": 0
          },
          // {
          //   "quadrant": 3,
          //   "ring": 0,
          //   "label": "Kafka",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          // {
          //   "quadrant": 3,
          //   "ring": 0,
          //   "label": "Nakadi",
          //   "link": "",
          //   "active": true,
          //   "moved": 0
          // },
          {
            "quadrant": 3,
            "ring": 1,
            "label": "RabbitMQ",
            "link": "",
            "active": true,
            "moved": 0
          }
        ]

      }
    }
  },
  mounted() {

  },
  methods: {
    // toggle modal methods will be one method with an extra var - a switch
    togglePropositionFormModal() {
      this.emitter.emit("toggle-proposition-form-modal", {
        displayed: !this.propFormDisplay,
      });
    },
    toggleTechListModal() {
      this.emitter.emit("toggle-tech-list-modal", {
        displayed: !this.techListDisplay,
      });
    },
    toggleInstructionModal() {
      this.emitter.emit("toggle-instruction-modal", {
        displayed: !this.instructionDisplay,
      });
    },
  }
}
</script>
