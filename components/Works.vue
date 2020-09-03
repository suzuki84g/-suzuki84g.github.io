<template>
  <div class="works row">
    <h2 class="col-12">
      Works
    </h2>
    <div v-for="work in works" :key="work" class="col-12">
      <ul>
        <li>{{ work.title }}</li>
        <li>{{ work.url }}</li>
        <li>{{ work.src }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      works: [
        { title: 'ポートフォリオ', url: 'https://suzuki84g.github.io/', src: 'https://github.com/suzuki84g/suzuki84g.github.io' },
        { title: 'イカステージ', url: 'https://ika-stage.herokuapp.com/index.html', src: 'https://github.com/suzuki84g/ikaStageSort' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
