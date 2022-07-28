<template>
  <div class="home">
    <h1>Home</h1>
    <CustomText tag="p" size="xsmall">Merhaba DÜnya</CustomText>
    <IconHome />
  </div>
</template>

<script>
import CustomText from '@/components/CustomText'
import IconHome from '../../icons/home.svg'

export default {
  name: 'HomeView',
  components: {
    CustomText,
    IconHome
  }
}
</script>
