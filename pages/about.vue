<template>
  <div class="container mx-16 mt-8">
    <h1 class="text-6xl">
      {{ title }}
    </h1>
    <p class="text-2xl">
      {{ body }}
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'How to make 10 figures a day',
      body: 'Here we have plenty things here'
    }
  }
}
</script>
