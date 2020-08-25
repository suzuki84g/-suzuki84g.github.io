<template>
  <div>
    <Profile />
    <Portfolio />
    <History />
    <Topix />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import Portfolio from '~/components/Portfolio'
import History from '~/components/History'
import Topix from '~/components/Topix'

export default {
  components: {
    Profile,
    Portfolio,
    History,
    Topix
  }
}
</script>

<style lang="scss">
</style>
