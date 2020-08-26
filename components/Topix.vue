<template>
  <div class="topix">
    <h2>Topix</h2>
    <div v-for="topix in topix" :key="topix.title">
      <span>{{ topix.title }} {{ topix.value }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      topix: [
        { title: '子供2人', value: '娘9歳と息子7歳' },
        { title: 'ゲーム', value: 'splatoon2/APEX' },
        { title: '料理', value: 'カレーをスパイスから作る' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
