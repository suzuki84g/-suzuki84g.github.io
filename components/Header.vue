<template>
  <div class="header">
    <div class="page-title">
      <h1>ポートフォリオ</h1>
    </div>
    <div class="navlist">
      <p>更新日付とか</p>
    </div>
    <!-- <Navlist /> -->
  </div>
</template>

<script>
// import Navlist from '~/components/Navlist'

export default {
  components: {
    // Navlist
  }
}
</script>

<style lang="scss">
.header {
  background-color: $background-gray;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 15px;
  .navlist {
  }
}
</style>
