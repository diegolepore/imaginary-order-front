<template>
  <div class="grid grid-cols-1 lg:grid-cols-4 gap-8">
    <div class="md:col-span-1 flex justify-center">
      <img class="w-2/4 lg:w-full" src="https://images.unsplash.com/photo-1584446922442-7ac6b8c118f3?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=993&q=80" alt="">
    </div>
    <div class="md:col-span-3">
      <h2 class="text-2xl md:text-3xl mb-4">{{ title }}</h2>
      <p> {{ excerpt }} </p>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      excerpt: {
        type: String,
        required: true
      } 
    }
  }
</script>

<style lang="scss" scoped>

</style>