<template>
  <div>
    <h1 class="text-4xl md:text-7xl text-center mt-8 mb-16 border-b-2 pb-8">Orden imaginario</h1>
    
    <div>
      <ul class="pb-32">
        <li v-for="post in posts" :key="post.id" class="mb-24">
          <nuxt-link :to="`/post/${post.id}`">
            <PostItem :title="post.title" :excerpt="post.excerpt" />
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const posts = await $axios.get('https://imaginary-order-app.herokuapp.com/posts')
    return {
      posts: posts.data
    }
  }
}
</script>

<style>
</style>
