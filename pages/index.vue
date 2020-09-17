<template>
  <div class="container">
    <Profile />
    <Skills />
    <Works />
    <!-- <History /> -->
    <!-- <Images /> -->
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import Skills from '~/components/Skills'
import Works from '~/components/Works'
// import History from '~/components/History'
// import Images from '~/components/Images'

export default {
  components: {
    Profile,
    Skills,
    Works
    // History,
    // Images,
  }
}
</script>

<style lang="scss">
</style>
