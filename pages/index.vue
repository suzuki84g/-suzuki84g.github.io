<template>
  <v-container fluid>
    <Profile />
    <Skills />
    <History />
    <!-- <Images /> -->
    <Works />
    <Link />
  </v-container>
</template>

<script>
import Profile from '~/components/Profile'
import Skills from '~/components/Skills'
import History from '~/components/History'
// import Images from '~/components/Images'
import Works from '~/components/Works'
import Link from '~/components/Link'

export default {
  components: {
    Profile,
    Skills,
    History,
    // Images,
    Works,
    Link
  }
}
</script>

<style lang="scss">
</style>
