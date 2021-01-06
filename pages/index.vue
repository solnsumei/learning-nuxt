<template>
  <div class="container flex items-center mx-auto justify-center mt-8">
    <div>
      <Logo />
      <h1 class="text-7xl mb-6">
        learning-nuxt
      </h1>
      <div class="w-full flex">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="border-teal-400 rounded border-2 px-4 py-2"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="border-teal-400 rounded border-2 px-4 py-2 ml-4"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return {
      title: 'Home Page'
    }
  }
}
</script>
