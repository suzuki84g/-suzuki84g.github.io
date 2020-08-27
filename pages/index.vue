<template>
  <div>
    <Profile />
    <History />
    <Topix />
    <Images />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import History from '~/components/History'
import Topix from '~/components/Topix'
import Images from '~/components/Images'

export default {
  components: {
    Profile,
    History,
    Topix,
    Images
  }
}
</script>

<style lang="scss">
</style>
