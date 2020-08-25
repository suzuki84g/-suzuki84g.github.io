<template>
  <div class="container">
    <Portfolio />
  </div>
</template>

<script>
import Portfolio from '~/components/Portfolio'

export default {
  components: {
    Portfolio
  }
}
</script>

<style lang="scss">
.container {
  display: flex;
  flex-direction: column;
}
</style>
