<template>
  <div>
    <Navbar/>
    <nuxt/>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar';
export default {
  components: {
    Navbar
  }
};
</script>

<style lang="scss">
@import '~assets/sass/main';
</style>
