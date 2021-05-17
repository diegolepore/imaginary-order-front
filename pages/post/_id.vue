<template>
  <div class="mb-32" v-if="post">
    <h1 class="text-4xl md:text-7xl text-center mt-8 mb-16 border-b-2 pb-8"> {{ post.title }} </h1>
    <div class="mb-8">
      <img class="w-100" src="https://images.unsplash.com/photo-1584446922442-7ac6b8c118f3?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=993&q=80" alt="">
    </div>
    <div v-html="$md.render(post.content)"></div>
  </div>
</template>

<script>
  export default {
    async asyncData({ params, $axios }) {
      const id = params.id
      const post = await $axios.get(`https://imaginary-order-app.herokuapp.com/posts/${id}`)

      return {
        id,
        post: post.data
      }
    },
    validate({ params }) {
      return !!params.id
    }
  }
</script>

<style lang="scss" scoped>

</style>