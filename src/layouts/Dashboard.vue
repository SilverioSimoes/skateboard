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
    <div class="p-5 flex-1">
      <header class="flex items-center justify-between">
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

      <h1 class="font-bold text-4xl mt-6 mb-4">Discover</h1>

      <div class="grid grid-cols-12">
        <div class="rounded-xl col-span-8 h-64 border border-red-500">
          <img
            src="https://via.placeholder.com/2000x1400"
            alt=""
            class="object-cover"
          />
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

export default {
  name: 'Dashboard',
  components: {
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
