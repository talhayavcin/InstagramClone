<template>
  <div class="home">
    <h1>Home</h1>
    <CustomText>Merhaba DÜnya</CustomText>
  </div>
</template>

<script>
import CustomText from '@/components/CustomText'

export default {
  name: 'HomeView',
  components: {
    CustomText
  }
}
</script>

<style>
h1 {
  color: red;
}
</style>
