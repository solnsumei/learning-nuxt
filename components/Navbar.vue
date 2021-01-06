<template>
  <div>
    <nav class="flex justify-between px-6 lg:px-16 items-start py-4">
      <div class="container">
        <a href="#" class="text-3xl text-green-500 font-light">
          Nuxt Fundamentals
        </a>
        <span class="block text-lg">A vue training</span>
      </div>
      <div class="text-right">
        <NuxtLink to="/posts" class="font-light">
          Posts
        </NuxtLink>
      </div>
    </nav>
  </div>
</template>

<script>
export default {}
</script>
