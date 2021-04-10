<template>
  <div class="container c-wrapper">
    <cTopBar />
    <div class="c-topmain flex space-between">
      <cRoulette />
      <cSidebar />
    </div>
    <cKeyboard />
  </div>
</template>

<script>
import cTopBar from '@/components/CTopBar.vue'
import cRoulette from '@/components/CRoulette.vue'
import cSidebar from '@/components/CSidebar.vue'
import cKeyboard from '@/components/CKeyboard.vue'

  export default {
    name: 'index',
    components: {
      cTopBar,
      cRoulette,
      cSidebar,
      cKeyboard
    }
  }
</script>