<template>
  <div class="app">
    <MasterHeader />

    <main class="main">
      <ContainerPart>
        <router-view />
      </ContainerPart>
    </main>
  </div>
</template>

<script>
import MasterHeader from '@/components/HeaderPart'
import ContainerPart from './components/ContainerPart.vue'
export default {
  name: 'App',
  components: {
    MasterHeader,
    ContainerPart
  }
}
</script>

<style scoped>
.main {
  padding-top: 40px;
}
</style>
