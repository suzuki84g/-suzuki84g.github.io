<template>
  <div class="container">
    <Profile />
    <Skills />
    <Works />
    <!-- <Timeline /> -->
    <!-- <Images /> -->
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import Skills from '~/components/Skills'
import Works from '~/components/Works'
// import Timeline from '~/components/Timeline'
// import Images from '~/components/Images'

export default {
  components: {
    Profile,
    Skills,
    Works
    // Timeline
    // Images,
  }
}
</script>

<style lang="scss">
</style>
