<template
  ><section class="text-gray-700 body-font bg-gray-200">
    <div
      class="container mx-auto flex flex-col px-5 py-12 justify-center items-center"
    >
      <div class="w-full md:w-2/3 flex flex-col items-center text-center">
        <h1
          class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"
        >
          Subscribe for Updates!
        </h1>
        <form
          id="subscribeForm"
          name="subscribe"
          method="POST"
          data-netlify="true"
          action="/form/success"
          class="flex w-full justify-center"
        >
          <input
            class="border-0 bg-gray-100 rounded mr-4 border border-gray-400 focus:outline-none focus:border-green-500 text-base px-4 lg:w-full xl:w-1/3 w-2/4 md:w-full"
            placeholder="Email"
            type="email"
            required="required"
          />
          <button
            type="submit"
            class="inline-flex text-white bg-green-500 border-0 py-2 px-6 focus:outline-none hover:bg-green-600 rounded text-lg"
          >
            Submit
          </button>
        </form>
        <p class="text-sm mt-2 text-gray-600 mb-4 w-full">
          Don't worry, You won't be spammed! <br />
          Because I can't afford to.
        </p>
        <Creator />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Footer',
  props: {},

  data: () => ({}),

  methods: {},
}
</script>
<style lang="postcss" scoped></style>
