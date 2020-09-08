<template>
  <v-row class="works">
    <v-col cols="12" class="row-title">
      Works
    </v-col>
    <v-card v-for="work in works" :key="work">
      <v-card-title>{{ work.title }}</v-card-title>
      <v-card-text>
        <p>{{ work.about }}</p>
        <p><a :href="work.url">{{ work.url }}</a></p>
        <p><a :href="work.code">github</a></p>
      </v-card-text>
    </v-card>
  </v-row>
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
</style>
