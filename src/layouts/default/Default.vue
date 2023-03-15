<template>
  <v-app class="tw-bg-[#efefef] tw-h-screen">
    <v-navigation-drawer
      class="tw-w-1/4"
      color="grey-lighten-3"
      rail
      v-model="showSidebar"
      location="right"
    >
      <div class="tw-h-36 tw-bg-blue-800 tw-p-5 tw-flex tw-items-start">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="tw-w-16 tw-h-16 tw-text-white">
  <path d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
</svg>
 <span class="tw-text-white tw-uppercase tw-text-3xl tw-ml-2">Lucas Design Studio</span>
      
    <div @click="showSidebar = !showSidebar"
    :class="showSidebar ? ' -tw-left-10' : ' -tw-left-16'"
     class="tw-h-16 tw-bg-sky-700 tw-absolute tw-px-1 tw-flex tw-items-center">
    <svg v-if="showSidebar" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="tw-w-8 tw-h-8 tw-text-gray-400">
    <path fill-rule="evenodd" d="M7.5 3.75A1.5 1.5 0 006 5.25v13.5a1.5 1.5 0 001.5 1.5h6a1.5 1.5 0 001.5-1.5V15a.75.75 0 011.5 0v3.75a3 3 0 01-3 3h-6a3 3 0 01-3-3V5.25a3 3 0 013-3h6a3 3 0 013 3V9A.75.75 0 0115 9V5.25a1.5 1.5 0 00-1.5-1.5h-6zm10.72 4.72a.75.75 0 011.06 0l3 3a.75.75 0 010 1.06l-3 3a.75.75 0 11-1.06-1.06l1.72-1.72H9a.75.75 0 010-1.5h10.94l-1.72-1.72a.75.75 0 010-1.06z" clip-rule="evenodd" />
    </svg>
    <svg v-else xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="tw-w-8 tw-h-8 tw-text-gray-400">
  <path fill-rule="evenodd" d="M7.5 3.75A1.5 1.5 0 006 5.25v13.5a1.5 1.5 0 001.5 1.5h6a1.5 1.5 0 001.5-1.5V15a.75.75 0 011.5 0v3.75a3 3 0 01-3 3h-6a3 3 0 01-3-3V5.25a3 3 0 013-3h6a3 3 0 013 3V9A.75.75 0 0115 9V5.25a1.5 1.5 0 00-1.5-1.5h-6zm5.03 4.72a.75.75 0 010 1.06l-1.72 1.72h10.94a.75.75 0 010 1.5H10.81l1.72 1.72a.75.75 0 11-1.06 1.06l-3-3a.75.75 0 010-1.06l3-3a.75.75 0 011.06 0z" clip-rule="evenodd" />
</svg>

    </div>
      </div>
      <v-expansion-panels class="tw-p-4">
      <v-expansion-panel>
        <v-expansion-panel-title class="tw-font-bold tw-text-base tw-px-1">
          <v-icon color="error" icon="mdi-heart" class="tw-mr-1"></v-icon>
          Visualizer Selections
          <span class="tw-ml-auto tw-rounded-full tw-bg-teal-200 tw-text-center tw-w-8">1</span>
        </v-expansion-panel-title>
        <v-expansion-panel-text>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-text>
      </v-expansion-panel>
      </v-expansion-panels>

      <!-- <v-card> -->
        <v-tabs
          v-model="tab"
          :show-arrows="false" 
          :hide-slider="true"
          class="tw-drop-shadow-xs tw-text-xs tw-px-0"
          density="compact"
        >
          <v-tab value="1" :class="tab == 1 ? '' : 'tw-bg-[#d1d1d1]'" class="tw-font-bold tw-text-xs">
            Living Room
          </v-tab>

          <v-tab value="2"  :class="tab == 2 ? '' : 'tw-bg-[#d1d1d1]'"
           class="tw-font-bold tw-text-xs">
            Kitchen
          </v-tab>

          <v-tab value="3" :class="tab == 3 ? '' : 'tw-bg-[#d1d1d1]'" class="tw-font-bold tw-text-xs">
            Bath
          </v-tab>
        </v-tabs>

       <div class="tw-flex tw-p-4 tw-justify-between tw-items-center">
        <span class="tw-font-bold tw-mr-4 tw-text-base">Selections:</span>
        <div class="tw-flex tw-justify-between tw-w-2/3 tw-mr-2">
          <v-btn class="tw-px-2 tw-w-4/6 tw-bg-[#1063c7] tw-font-bold tw-text-white" :rounded="0"  prepend-icon="mdi-refresh">
          Reset All
        </v-btn>
        <v-divider
      class="ms-3"
      inset
      vertical :thickness="2"
    ></v-divider>
        <!-- <v-divider class="tw-text-dark tw-w-1" :thickness="2" color="dark" vertical></v-divider> -->
               <v-btn flat :rounded="0" color="white" prepend-icon="mdi-heart">
        </v-btn>
        </div>

       </div>

            <v-card class="tw-h-full tw-bg-inherit tw-rounded-0">
              <v-expansion-panels  class="tw-p-4 tw-rounded-0 tw-mb-2">
                <v-expansion-panel v-for="(section, index) in currentTabSections" :key="index" class="tw-mb-4">
                <v-expansion-panel-title class="tw-font-bold tw-text-lg tw-pl-4 tw-pr-2">
                  {{section.name}}
                </v-expansion-panel-title>
                <v-expansion-panel-text>
                <v-item-group v-model="group" :multiple="false" >
        <v-item v-for="(wall, index) in walls" :key="index"  #default="{ active, toggle }">
          <v-switch color="primary" inset @change="switchImage()" :label="wall.name" :input-value="active" hide-details ></v-switch>
        </v-item>

      </v-item-group>
                </v-expansion-panel-text>
              </v-expansion-panel>
              </v-expansion-panels>
            </v-card>

    </v-navigation-drawer>

    <v-main>
      <div>
        <div ref="preview" :class="showSidebar ? 'tw-w-3/4' :'tw-w-full'" class=" tw-relative tw-h-screen">

        </div>
    <vue-easy-lightbox
      :visible="true"
      :imgs="currentImage"
      :index="indexRef"
      :teleport="preview"
      :minZoom="1"
      :rotateDisabled="true"
      :escDisabled="true"
      :scrollDisabled="true"
      :moveDisabled="false"
      :maskClosable="false"
    />
  </div>

      <!-- <div>
    <button @click="showSingle">Show single picture.</button>
    <button @click="showMultiple">Show a group of pictures.</button>

    <vue-easy-lightbox
      :visible="visibleRef"
      :imgs="imgsRef"
      :index="indexRef"
      @hide="onHide"
    ></vue-easy-lightbox>
  </div> -->
      <!-- <v-img
      class="tw-my-auto tw-scale-150"
  aspect-ratio="16/9"
  cover
  src="@/assets/img/Walls-1.jpeg"
></v-img> -->
    <!-- <default-view /> -->
    </v-main>

  </v-app>
</template>

<script lang="ts" setup>
// If VueApp is already registered with VueEasyLightbox, there is no need to register it here.
// import VueEasyLightbox from 'vue-easy-lightbox'
import VueEasyLightbox, { useEasyLightbox } from 'vue-easy-lightbox'
  import { ref, computed } from 'vue'
  import firstImg from '@/assets/img/Walls-1.jpeg'
  import secondImg from '@/assets/img/Walls-2.jpeg'
  import thirdImg from '@/assets/img/Walls-3.jpeg'
//   const props = defineProps({
//   foo: String
// })

const {
      // methods
      show, onHide, changeIndex,
      // refs
      visibleRef, indexRef, imgsRef
    } = useEasyLightbox({
      // src / src[]
      imgs: 'https://i.loli.net/2018/11/10/5be6852cdb002.jpeg',
      // initial index
      initIndex: 0
    })
  
    const currentImage = ref(firstImg)
    const currentImageIndex = ref(1)
    const preview = ref(null)

    const switchImage = () => {
      console.log('switchImage called')
      if(currentImageIndex.value == 1){
        currentImage.value = secondImg
        currentImageIndex.value = 2
        return
  }
  if(currentImageIndex.value == 2){
    currentImage.value = thirdImg
    currentImageIndex.value = 3
    return
  }
  if(currentImageIndex.value == 3){
    currentImage.value = firstImg
    currentImageIndex.value = 1
    return

  }
    }


const tab =  ref(1)
const text = ref('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
const showSidebar = ref(true)
const group = ref(0)

const tabLivingRoom = ref([
  {
    name: 'Walls'
  },
  {
    name: 'Floors'
  },
  {
    name: 'Mantels'
  },
  {
    name: 'Tiles and Stones'
  },
])

const tabKitchen = ref([
  {
    name: 'Kitchen'
  },
  {
    name: 'Flooring'
  },
  {
    name: 'Wall Paint'
  },
  {
    name: 'Countertop'
  },
  {
    name: 'Cabinets'
  },
  {
    name: 'Cabinet Hardware'
  },
  {
    name: 'Island Cabinets'
  },
  {
    name: 'Backsplash'
  },
  {
    name: 'Appliances'
  },
])

const tabBath = ref([
  {
    name: 'Flooring'
  },
  {
    name: 'Shower Mosaic Floor'
  },
  {
    name: 'Wall Paint'
  },
  {
    name: 'Wall Tile'
  },
  {
    name: 'Countertop'
  },
  {
    name: 'Cabinets'
  },
  {
    name: 'Cabinet Hardware'
  },
])

const currentTabSections = computed(()=> {
  if(tab.value == 1){
    return tabLivingRoom.value
  }
  if(tab.value == 2){
    return tabKitchen.value
  }
  if(tab.value == 3){
    return tabBath.value
  }
  return []
})

const walls = ref([
  {
    name: 'SW6252 Ice Cube',
    img: 'Walls-1.jpeg',
    order: 1,
    selected: false
  },
  {
    name: 'SW7004 Snowbound',
    img: 'Walls-2.jpeg',
    order: 2,
    selected: false
  },  {
    name: 'SW7014 Eider White',
    img: 'Walls-3.jpeg',
    order: 3,
    selected: false
  },
])

</script>

<style>
.v-tab__slider, .v-slide-group__prev, .v-slide-group__next, .btn__close {
  display: none !important;
}
.vel-modal {
  position: unset !important;
}
</style>