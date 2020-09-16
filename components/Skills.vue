<template>
  <div class="content">
    <div class="title">
      <h2>Skill</h2>
    </div>
    <div class="mainContainer">
      <div class="front">
        <p>フロント技術</p>
        <p v-for="front in skillSet.front" :key="front">
          {{ front }}
        </p>
      </div>
      <div class="backend">
        <p>サーバサイド技術</p>
        <p v-for="back in skillSet.back" :key="back">
          {{ back }}
        </p>
      </div>
      <div class="other">
        <p>その他、インフラや開発ツール</p>
        <p v-for="other in skillSet.other" :key="other">
          {{ other }}
        </p>
      </div>
    </div>
  </div>
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
