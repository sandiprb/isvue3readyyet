<template>
  <div>
    <div class="text-center py-16 md:py-24 container">
      <Logo />
      <div class="text-3xl text-center text-secondary">Is Vue3 ready yet?</div>
      <div class="font-bold text-12x">{{ status }}</div>
    </div>
    <FrameworkParts />
    <Footer />
  </div>
</template>

<script>
export default {
  data: () => ({
    status: 'YES',
  }),
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
