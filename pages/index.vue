<template>
  <div>
    <Profile />
    <History />
    <Images />
    <Skills />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import History from '~/components/History'
import Images from '~/components/Images'
import Skills from '~/components/Skills'

export default {
  components: {
    Profile,
    History,
    Images,
    Skills
  }
}
</script>

<style lang="scss">
</style>
