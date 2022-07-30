<template>
  <div class="home">
    <CustomText tag="p" size="xsmall">Profile</CustomText>
    <div id="nav">
      <router-link to="/profile">Post</router-link> |
      <router-link to="/profile/igtv">IGTV</router-link> |
      <router-link to="/profile/save">Save</router-link> |
      <router-link to="/profile/tag">Tag</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import CustomText from '@/components/CustomText'

export default {
  name: 'ProfilePart',
  components: {
    CustomText
  }
}
</script>
