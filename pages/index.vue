<template>
  <div class="container">
    <Profile />
    <Skills />
    <!-- <History /> -->
    <!-- <Images /> -->
    <!-- <Works /> -->
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import Skills from '~/components/Skills'
// import History from '~/components/History'
// import Images from '~/components/Images'
// import Works from '~/components/Works'

export default {
  components: {
    Profile,
    Skills
    // History,
    // Images,
    // Works
  }
}
</script>

<style lang="scss">
</style>
