<template>
  <div class="header">
    <div class="title">
      <h1>ポートフォリオ</h1>
    </div>
    <div>
      <Navlist />
    </div>
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
  flex-direction: row;
  justify-content: space-between;
  h1 {
    font: {
      weight: bold;
    }
  }
  div:last-child {
    align-self: flex-end;
  }
}
</style>
