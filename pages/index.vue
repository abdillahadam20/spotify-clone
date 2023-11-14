<template>
  <div class="w-full bg-spotify-black rounded-lg relative">
    <div class="absolute top-0 z-50">
      <div>
        <nuxt-link to="">
          <icon name="material-symbols:arrow-back-ios-rounded" />
        </nuxt-link>
        <nuxt-link to="">
          <icon name="material-symbols:arrow-forward-ios-rounded" />
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="">Sign up</nuxt-link>
        <UButton label="Log in" color="black" variant="solid" :ui="{ rounded: 'rounded-full' }" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>