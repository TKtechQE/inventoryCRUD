<template>
  <div class="home">
    <div class="container">
      <hello-world msg="recs"/>
      <parts-grid />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import PartsGrid from '@/components/PartsGrid.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    PartsGrid
  }
}
</script>
