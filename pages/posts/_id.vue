<template>
  <div class="container px-6 lg:px-16 grid md:grid-cols-4">
    <div class="col-span-3 pb-2">
      <div v-if="post">
        <h1 class="text-2xl text-green-600 font-light">
          {{ post.title }}
        </h1>
        <p>{{ post.body }}</p>
        <p class="mt-4">
          <NuxtLink to="/posts">
            Back
          </NuxtLink>
        </p>
      </div>
      <div v-else>
        <h1 class="text-2xl text-green-600 font-light">
          Posts
        </h1>
        <ul>
          <li v-for="item in posts" :key="item.id">
            <NuxtLink :to="`/posts/${item.id}`">
              {{ item.title }}
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
    <aside v-if="post" class="col-span-1 ml-0 lg:ml-4">
      <h1 class="text-2xl text-green-600 font-light">
        Related Posts
      </h1>
      <ul>
        <li v-for="related in relatedPosts" :key="related.id">
          <NuxtLink :to="{name: 'posts-id', params: {id: related.id}}">
            {{ related.title }}
          </NuxtLink>
        </li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  data () {
    return {
      id: this.$route.params.id,
      posts: this.$store.state.posts.all
    }
  },
  computed: {
    post () {
      return this.posts.find(post => post.id === parseInt(this.id))
    },
    relatedPosts () {
      return this.posts.filter(post => post.id !== parseInt(this.id))
    }
  },
  head () {
    return {
      title: `Posts | ${this.post ? this.post.title : 'Home'}`
    }
  }
}
</script>
