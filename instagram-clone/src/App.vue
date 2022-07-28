<template>
  <div class="app">
    <MasterHeader />
    <router-view />
  </div>
</template>

<script>
import MasterHeader from '@/components/HeaderPart'
export default {
  name: 'App',
  components: {
    MasterHeader
  }
}
</script>
