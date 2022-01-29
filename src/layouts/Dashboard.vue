import { HomeIcon } from '@heroicons/vue/solid';
<template>
  <div class="bg-gray-800 flex text-white max-h-screen h-screen">
    <div class="w-64">
      <span class="font-semibold px-6 py-3 block">Skateboard</span>

      <nav class="p-6">
        <h3>Menu</h3>

        <div class="flex items-center">
          <div class="bg-orange-500"><HomeIcon /></div>

          <span>Discover</span>
        </div>
      </nav>
    </div>
    <div class="border-2 flex-1 border-red-500">
      <HomeIcon class="h-5 inline" />Content
    </div>
  </div>
</template>

<script>
import HomeIcon from '../components/icons/HomeIcon.vue'

export default {
  name: 'Dashboard',
  components: { HomeIcon }
}
</script>

<style></style>
