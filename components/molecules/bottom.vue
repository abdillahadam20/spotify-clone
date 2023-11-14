<template>
 <div class="flex flex-col justify-center items-start w-[450px] bg-spotify-black rounded-lg px-6 py-6 gap-4">
      <div class="flex justify-between w-full h-16 items-center">
        <nuxt-link to="#" class="flex justify-center items-center gap-4 text-base font-semibold opacity-70 transition-all ease-in-out duration-300 hover:opacity-100">
          <icon name="fluent:library-20-filled" size="24" />
          <span>Your Library</span>
        </nuxt-link>
        <nuxt-link to="#">
          <icon name="iconamoon:sign-plus" size="24" class="flex justify-center items-center gap-4 text-base w-8 h-8 font-semibold opacity-70 transition-all ease-in-out duration-300 hover:opacity-100 hover:w-8 hover:h-8 hover:rounded-full hover:bg-spotify-eval hover:text-opacity-50" />
        </nuxt-link>
      </div>
      <div class="w-full flex flex-col gap-4 justify-center items-start overflow-auto mb-[5rem]">
        <div class="bg-spotify-eval w-full px-4 py-5 rounded-lg flex flex-col gap-3 justify-center items-start">
          <h3 class="font-semibold text-base">Create your first playlist</h3>
          <p class="font-normal text-sm">It's easy, we'll help you</p>
          <UButton :ui="{ rounded: 'rounded-full'}" color="black" variant="solid">Create Playlist</UButton>
        </div>
        <div class="bg-spotify-eval w-full px-4 py-5 rounded-lg flex flex-col gap-3 justify-center items-start">
          <h3 class="font-semibold text-base">Let's find some poadcasts to follow</h3>
          <p class="font-normal text-sm">we'll keep you update on new episodes</p>
          <UButton :ui="{ rounded: 'rounded-full'}" color="black" variant="solid">Browse poadcasts</UButton>
        </div>
      </div>
      <div class="flex flex-col justify-center items-start gap-2">
        <ul class="flex flex-wrap gap-[12px] text-[#a7a7a7] text-[11px] w-full" >
        <li v-for="link, index in data.link" :key="index">
          <nuxt-link :to="link.link" class="w-full">{{ link.title }}</nuxt-link>
        </li>
      </ul>
      <nuxt-link to="" class="text-[#a7a7a7] text-[11px]">Cookies</nuxt-link>
      <UButton
      :ui="{ rounded: 'rounded-full' }"
  icon="i-heroicons-globe-alt"
  color="black"
  variant="outline"
  label="English"
  :trailing="false"
/>

      </div>
    </div>
</template>

<script setup lang="ts">
interface ILink {
  title: string
  link: string
}

const data = reactive<{
  link: ILink[]
}>({
  link: [
  {
    title: 'Legal',
    link: '#'
  },
  {
    title: 'Privacy Center',
    link: '#'
  },
  {
    title: 'Privacy Policy',
    link: '#'
  },
  {
    title: 'Cookies',
    link: '#'
  },
  {
    title: 'About Ads',
    link: '#'
  },
  {
    title: 'Accessibility',
    link: '#'
  }
  ]
})


</script>

<style scoped>

</style>