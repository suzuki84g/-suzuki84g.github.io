<template>
  <div>
    <Profile />
    <History />
    <Images />
    <Skills />
    <Works />
    <Link />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import History from '~/components/History'
import Images from '~/components/Images'
import Skills from '~/components/Skills'
import Works from '~/components/Works'
import Link from '~/components/Link'

export default {
  components: {
    Profile,
    History,
    Images,
    Skills,
    Works,
    Link
  }
}
</script>

<style lang="scss">
</style>
