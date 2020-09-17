<template>
  <section>
    <div class="title">
      <h2>Works</h2>
    </div>
    <div class="works-container">
      <div v-for="work in works" :key="work" class="work">
        <p>{{ work.title }}</p>
        <p>{{ work.overview }}</p>
        <p><a :href="work.url">{{ work.url }}</a></p>
        <p><a :href="work.code">github</a></p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      works: [
        {
          title: 'ポートフォリオ',
          overview: 'このポートフォリオです。',
          // image: require(),
          url: 'https://suzuki84g.github.io/',
          code: 'https://github.com/suzuki84g/suzuki84g.github.io',
          tech: [],
          impressions: ''
        },
        {
          title: 'イカステージ',
          overview: 'splatoon2のステージ情報を表示します。',
          // image: require(),
          url: 'https://ika-stage.herokuapp.com/index.html',
          code: 'https://github.com/suzuki84g/ikaStageSort',
          tech: [],
          impressions: ''
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.works-container {
  display: flex;
  flex-direction: column;
  .work {
    margin-bottom: 1rem;
  }
}
</style>
