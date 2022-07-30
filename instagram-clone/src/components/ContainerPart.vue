<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'ContainerPart'
}
</script>

<style scoped>
.container {
  max-width: 940px;
  margin-left: auto;
  margin-right: auto;
}
</style>
