<template>
  <nav class="px-3 py-2 h-screen flex flex-col gap-2">
    <molecules-top />
    <molecules-bottom />
  </nav>
</template>

<script setup lang="ts">
const isActive = ref(false)
</script>

<style scoped lang="postcss">
.navbar {
  @apply px-3 py-2 h-screen;

  &-top {
    @apply flex flex-col justify-center items-start w-[450px] bg-spotify-black rounded-lg px-6 py-6 gap-4;

    &-logo {
      @apply flex justify-center items-center gap-1 text-base font-semibold;
    }

    &-menu {
      ul {
        @apply flex flex-col justify-center items-start gap-6;

        li {
          a {
            @apply flex justify-center items-center gap-4 text-base font-semibold opacity-70 transition-all ease-in-out duration-300;

            &:hover {
              @apply opacity-100;
            }
          }
        }
      }
    }
  }

  &-bottom {
    @apply flex flex-col justify-center items-start w-[450px] h-48 bg-spotify-black rounded-lg px-6 py-6 gap-4;

    &-library {
      @apply flex justify-between;
    }
  }
}
</style>