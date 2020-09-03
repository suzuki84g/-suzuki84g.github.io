<template>
  <div class="header">
    <h1 class="page-title">
      ポートフォリオ
    </h1>
    <Navlist />
  </div>
</template>

<script>
import Navlist from '~/components/Navlist'

export default {
  components: {
    Navlist
  }
}
</script>

<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
