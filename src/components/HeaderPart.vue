<template>
  <header class="header">
    <ContainerPart class="header-inner">
      <!--- Logo -->
      <router-link class="logo" to="/"> Instagram </router-link>

      <!--- Search-->
      <form class="search">
        <input type="text" placeholder="Search" />
      </form>

      <!--- Navigation-->
      <nav class="navigation">
        <router-link to="/">
          <IconHomeFill v-if="$route.name === 'Home'" />
          <IconHome v-else />
        </router-link>
        <router-link to="/direct">
          <IconDirectFill v-if="$route.name === 'Direct'" />
          <IconDirect v-else />
        </router-link>
        <router-link to="/explore">
          <IconExploreFill v-if="$route.name === 'Explore'" />
          <IconExplore v-else />
        </router-link>
        <router-link to="/profile">Profile</router-link>
      </nav>
    </ContainerPart>
  </header>
</template>

<script>
import IconHome from '@/icons/home.svg'
import IconHomeFill from '@/icons/home-fill.svg'
import IconDirect from '@/icons/direct.svg'
import IconDirectFill from '@/icons/direct-fill.svg'
import IconExplore from '@/icons/explore.svg'
import IconExploreFill from '@/icons/explore-fill.svg'
import ContainerPart from '@/components/ContainerPart'

export default {
  name: 'MainHeader',
  components: {
    IconHome,
    IconHomeFill,
    IconDirect,
    IconDirectFill,
    IconExplore,
    IconExploreFill,
    ContainerPart
  }
}
</script>

<style scoped>
.header {
  z-index: 90;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  background-color: white;
  border-bottom: 1px solid rgb(var(--b6a));
}
.header-inner {
  height: var(--header-height);
  display: flex;
  align-items: center;
  justify-content: center;
  @media (--t) {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
  }
}
.logo {
  font-size: 2rem;
  font-weight: bold;
}
.search {
  display: none;
  @media (--t) {
    display: block;
    text-align: center;
    input {
      width: 215px;
      height: 28px;
      border: 1px solid rgb(var(--b6a));
      background-color: rgb(var(--b3f));
      border-radius: 4px;
      padding-left: 20px;
      padding-right: 20px;
    }
  }
}
.navigation {
  z-index: 90;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: white;
  border-top: 1px solid rgb(var(--b6a));
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  @media (--t) {
    height: auto;
    border: 0;
    position: static;
    justify-content: flex-end;
    a {
      margin-left: 20px;
    }
  }
}
</style>
