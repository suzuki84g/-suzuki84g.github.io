<template>
  <div>
    <Profile />
    <Portfolio />
    <History />
  </div>
</template>

<script>
import Profile from '~/components/Profile'
import Portfolio from '~/components/Portfolio'
import History from '~/components/History'

export default {
  components: {
    Profile,
    Portfolio,
    History
  }
}
</script>

<style lang="scss">
</style>
