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
  async asyncData(){
    let status='NO';
    try{
      const response = await fetch('https://cors-anywhere.herokuapp.com/https://github.com/vuejs/vue-next/releases/tag/v3.0.0')
      if (response.status === 200){
        status = 'YES';
      }
    }
    catch(e){}
    return {status}
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
