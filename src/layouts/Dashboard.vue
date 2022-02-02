<template>
  <div class="bg-gray-800 flex text-white max-h-screen h-screen">
    <div class="w-64">
      <span class="font-semibold p-6 block opacity-90">Skateboard</span>

      <nav class="p-6">
        <h3
          class="opacity-50 uppercase font-semibold tracking-wider mb-6 text-xs"
        >
          Menu
        </h3>

        <div class="space-y-6">
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
        </div>
      </nav>
    </div>
    <div class="flex-1 h-screen relative overflow-y-auto">
      <header
        class="p-5 flex bg-gray-800 z-20 sticky top-0 items-center justify-between"
      >
        <InputSearch class="w-96" />

        <div class="flex items-center">
          <div class="flex items-center space-x-3 ml-5">
            <Avatar />

            <span>Thomas</span>
            <ChevronDownIcon class="w-4 h-4" />
          </div>

          <BellIcon
            class="w-5 h-5 ml-8 opacity-50 hover:opacity-100 cursor-pointer transition duration-100"
          />
        </div>
      </header>

      <div class="px-5 pb-5 content">
        <h1 class="font-bold text-4xl mt-6 mb-4">Discover</h1>

        <div class="grid gap-4 grid-cols-12">
          <div class="col-span-8 h-96 rounded-3xl overflow-hidden relative">
            <div class="flex w-full h-full">
              <img
                src="https://via.placeholder.com/2000x1400"
                alt=""
                class="w-full object-cover"
              />
              <div class="z-10 absolute top-0 p-6 bottom-0 w-full">
                <h3 class="text-2xl max-w-xs">
                  How to do Basic Jumping and how to landing to safely
                </h3>
                <p
                  class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 text-white"
                >
                  7 minutes
                </p>
              </div>
            </div>
          </div>

          <div class="col-span-4 h-96 rounded-3xl overflow-hidden relative">
            <div class="flex w-full h-full">
              <img
                src="https://via.placeholder.com/2000x1400"
                alt=""
                class="w-full object-cover"
              />
              <div class="z-10 absolute top-0 p-6 bottom-0 w-full">
                <h3 class="text-2xl max-w-xs">
                  How to do Basic Jumping and how to landing to safely
                </h3>
                <p
                  class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 text-white"
                >
                  7 minutes
                </p>
              </div>
            </div>
          </div>
        </div>

        <h1 class="text-2xl mt-6 mb-4">Most Watched</h1>

        <div class="grid grid-cols-4 gap-4">
          <CardItem v-for="n of 10" :key="n" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MenuItem from '../layouts/navs/MenuItem.vue'
import HomeIcon from '../components/icons/HomeIcon.vue'
import TrendingUpIcon from '../components/icons/TrendingUpIcon.vue'
import InputSearch from '../components/inputs/InputSearch.vue'
import Avatar from '../components/Avatar.vue'
import ChevronDownIcon from '../components/icons/ChevronDownIcon.vue'
import BellIcon from '../components/icons/BellIcon.vue'
import CardItem from '../components/CardItem.vue'

export default {
  name: 'Dashboard',
  components: {
    CardItem,
    MenuItem,
    HomeIcon,
    TrendingUpIcon,
    InputSearch,
    Avatar,
    ChevronDownIcon,
    BellIcon
  },
  setup() {
    return { MenuItem, HomeIcon, TrendingUpIcon, InputSearch }
  }
}
</script>
