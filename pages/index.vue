<template>
  <div>
    <Profile />
    <History />
    <Images />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import History from '~/components/History'
import Images from '~/components/Images'

export default {
  components: {
    Profile,
    History,
    Images
  }
}
</script>

<style lang="scss">
</style>
