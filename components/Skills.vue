<template>
  <v-row class="skill">
    <v-col cols="12" class="row-title">
      Skill
    </v-col>
    <v-card>
      <v-card-title>フロント技術</v-card-title>
      <v-card-text>
        <p v-for="front in skillSet.front" :key="front">
          {{ front }}
        </p>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-title>サーバサイド技術</v-card-title>
      <v-card-text>
        <p v-for="back in skillSet.back" :key="back">
          {{ back }}
        </p>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-title>その他、インフラや開発ツール</v-card-title>
      <v-card-text>
        <p v-for="other in skillSet.other" :key="other">
          {{ other }}
        </p>
      </v-card-text>
    </v-card>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      skillSet: {
        front: ['html', 'css/sass', 'javascript', 'Bootstrap', 'Vue.js', 'Nuxt.js', 'Vuetify'],
        back: ['Linux', 'WindowsServer', 'Python', 'Node.js', 'MySQL'],
        other: ['git', 'GitHub', 'docker', 'Vagrant', 'AWS', 'Heroku', 'PMO', 'オンプレミス環境の物理作業']
      }
    }
  }
}
</script>

<style lang="scss">
</style>
