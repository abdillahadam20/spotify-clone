<template>
  <div class="flex flex-col justify-center items-start w-[450px] bg-spotify-black rounded-lg px-6 py-6 gap-4">
      <nuxt-link to="#" class="flex justify-center items-center gap-1 text-base font-semibold">
          <icon name="simple-icons:spotify" size="24" />
          <span>Spotify</span>
        </nuxt-link>
      <div class="navbar-top-menu">
        <ul class="flex flex-col justify-center items-start gap-6">
          <li>
            <nuxt-link to="#" class="flex justify-center items-center gap-4 text-base font-semibold opacity-70 transition-all ease-in-out duration-300 hover:opacity-100">
              <icon name="bx:bxs-home" size="24" />
              <span>Home</span>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="#" class="flex justify-center items-center gap-4 text-base font-semibold opacity-70 transition-all ease-in-out duration-300 hover:opacity-100">
              <icon :name="isActive ? 'ph:magnifying-glass-fill' : 'ph:magnifying-glass-bold'" size="24" />
              <span>Search</span>
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
</template>

<script setup lang="ts">
const isActive = ref(false)
</script>

<style scoped>

</style>