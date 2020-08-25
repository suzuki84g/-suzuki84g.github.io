<template>
  <div>
    <Profile />
    <History />
    <Topix />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import History from '~/components/History'
import Topix from '~/components/Topix'

export default {
  components: {
    Profile,
    History,
    Topix
  }
}
</script>

<style lang="scss">
</style>
