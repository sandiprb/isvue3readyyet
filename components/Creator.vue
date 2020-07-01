<template>
  <div
    class="mb-8 md:mb-0 md:fixed opacity-75 hover:opacity-100"
    style="bottom: 1rem; right: 1rem;"
  >
    <div
      class="inline-flex items-center bg-gray-200 border-0 py-1 px-3 focus:outline-none hover:bg-gray-300 rounded text-base mt-4 md:mt-0"
    >
      <a
        href="https://github.com/sandiprb/isvue3readyyet"
        target="_blank"
        class="flex items-center text-xs"
      >
        <img src="@/assets/img/github.svg" alt="github logo" class="w-6 mr-1" />
        Source Code
      </a>
    </div>
    <div
      class="inline-flex items-center bg-gray-200 border-0 py-1 px-3 focus:outline-none hover:bg-gray-300 rounded text-base mt-4 md:mt-0"
    >
      <a
        href="https://twitter.com/sandip_rb"
        target="_blank"
        class="flex items-center text-xs"
      >
        <img
          src="@/assets/img/twitter.svg"
          alt="github logo"
          class="w-6 mr-1"
        />
        @sandip_rb
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Creator',
  props: {},

  data: () => ({}),

  methods: {},
}
</script>
<style lang="postcss" scoped></style>
