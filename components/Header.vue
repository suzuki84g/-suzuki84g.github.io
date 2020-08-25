<template>
  <div class="header">
    <div class="title">
      <h1>ポートフォリオ</h1>
    </div>
    <div>
      navlist
    </div>
  </div>
</template>

<script>
export default {}
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
