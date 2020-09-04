<template>
  <div class="works row justify-content-center">
    <h2 class="col-12">
      Works
    </h2>
    <div v-for="work in works" :key="work" class="card">
      <div class="card-body">
        <h4>{{ work.title }}</h4>
        <p>{{ work.about }}</p>
        <p><a :href="work.url">{{ work.url }}</a></p>
        <p><a :href="work.code">github</a></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      works: [
        {
          title: 'ポートフォリオ',
          about: 'このポートフォリオです。',
          url: 'https://suzuki84g.github.io/',
          code: 'https://github.com/suzuki84g/suzuki84g.github.io'
        },
        {
          title: 'イカステージ',
          about: 'splatoon2のステージ情報を表示します。',
          url: 'https://ika-stage.herokuapp.com/index.html',
          code: 'https://github.com/suzuki84g/ikaStageSort'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.card {
  width: 40%;
  margin: 0px 10px;
}
</style>
