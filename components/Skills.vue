<template>
  <div class="skill row justify-content-center">
    <h2 class="col-12">
      Skill
    </h2>
    <div class="col-sm-3">
      <p>フロント技術</p>
      <ul>
        <li v-for="front in skillSet.front" :key="front">
          {{ front }}
        </li>
      </ul>
    </div>
    <div class="col-sm-3">
      <p>サーバサイド技術</p>
      <ul>
        <li v-for="back in skillSet.back" :key="back">
          {{ back }}
        </li>
      </ul>
    </div>
    <div class="col-sm-3">
      <p>その他、インフラや開発ツール</p>
      <ul>
        <li v-for="other in skillSet.other" :key="other">
          {{ other }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      skillSet: {
        front: ['html', 'css/sass', 'javascript', 'Bootstrap', 'Vue.js', 'Nuxt.js'],
        back: ['Linux', 'WindowsServer', 'Python', 'Node.js', 'MySQL'],
        other: ['git', 'GitHub', 'docker', 'Vagrant', 'AWS', 'Heroku', 'オンプレミス環境の物理作業', 'PMOの真似事など']
      }
    }
  }
}
</script>

<style lang="scss">
</style>
