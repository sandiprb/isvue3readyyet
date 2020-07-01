<template>
  <section class="text-gray-700 body-font">
    <div class="container px-5 lg:py-24  mx-auto">
      <div class="flex flex-col text-center w-full mb-12">
        <h1 class="sm:text-3xl text-2xl font-medium title-font text-gray-900">
          Status of Major Framework Parts
        </h1>
      </div>
      <div class="flex flex-wrap -m-4">
        <div
          class="p-4 md:w-1/3"
          v-for="(item, index) in content"
          :key="`item-${index}`"
        >
          <div class="flex rounded-lg bg-gray-100 p-8 flex-col">
            <a :href="item.github" target="_blank">
              <div class="flex items-center mb-3">
                <div
                  class="w-8 h-8 mr-3 inline-flex items-center justify-center rounded-full text-white flex-shrink-0"
                >
                  <img
                    src="https://image.flaticon.com/icons/png/512/25/25231.png"
                    alt="github logo"
                  />
                </div>
                <h2 class="text-gray-900 text-lg title-font font-medium">
                  {{ item.title }}
                </h2>
              </div>
            </a>
            <a :href="item.npm" rel="nofollow" class="mb-4" target="_blank"
              ><img :src="item.badge" style="max-width: 100%;"
            /></a>

            <div class="flex-grow">
              <p class="leading-relaxed text-base" v-html="item.content"></p>
              <a
                class="mt-3 text-green-500 inline-flex items-center text-lg"
                :href="item.RFCs"
                v-show="item.RFCs"
                target="_blank"
                >RFCs
                <svg
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  class="w-4 h-4 ml-2"
                  viewBox="0 0 24 24"
                >
                  <path d="M5 12h14M12 5l7 7-7 7"></path>
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FrameworkParts',
  props: {},

  data: () => ({
    content: [
      {
        title: 'Vue 3 Core',
        github: 'https://github.com/vuejs/vue-next',
        RFCs: `https://github.com/vuejs/rfcs/pulls?q=is%3Apr+is%3Amerged+label%3Acore`,
        npm: `https://www.npmjs.com/package/vue/v/next`,
        badge: `https://camo.githubusercontent.com/35043cce2a552b9c29e6e2267f4c9c9baec31090/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f7675652f6e6578742e737667`,
        content: `Vue 3 core has been in beta for over two months now. We have merged all planned breaking change RFCs, and there are no further breaking changes planned before official 3.0 release.
        <br/>
        <br/>
        Thousands of early adopters have been using it for new projects and have helped us identify and fix many bugs and behavior inconsistencies with Vue 2. At this stage, we believe Vue 3 core is quite stable and ready for RC.`,
      },
      {
        title: 'Vue Router',
        github: 'https://github.com/vuejs/vue-router-next',
        RFCs: `https://github.com/vuejs/rfcs/pulls?q=is%3Apr+is%3Amerged+label%3Arouter`,
        npm: `https://www.npmjs.com/package/vue-router/v/next`,
        badge: `https://camo.githubusercontent.com/8c14172146de976291c555b24839bd6e7f65a3a7/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f7675652d726f757465722f6e6578742e737667`,
        content: `We still have a few minor router hook behavior consistency issues with <code> vue-router@3</code>.x, but these are the only things that is blocking the router from being marked as Beta. The router is usable for new, non-critical projects.`,
      },
      {
        title: 'Vuex',
        github: 'https://github.com/vuejs/vuex/tree/4.0',
        RFCs: ``,
        npm: `https://www.npmjs.com/package/vuex/v/next`,
        badge: `https://camo.githubusercontent.com/fbf0df4356b468846273e602cac7c43ef6fe7d5d/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f767565782f6e6578742e737667`,
        content: `The only difference between Vuex 4.0 and 3.x is that it's Vue 3 compatible! It is ready to enter RC together with Vue 3 core.`,
      },
    ],
  }),

  methods: {},
}
</script>
<style lang="postcss" scoped></style>
