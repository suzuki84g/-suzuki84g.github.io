<template>
  <div class="skill row justify-content-center">
    <h2 class="col-12">
      Skill
    </h2>
    <div class="col-10">
      <ul class="row">
        <li class="col-sm-4">
          フロント技術
          <ul>
            <li v-for="front in skillSet.front" :key="front">
              {{ front }}
            </li>
          </ul>
        </li>
        <li class="col-sm-4">
          サーバサイド技術
          <ul>
            <li v-for="back in skillSet.back" :key="back">
              {{ back }}
            </li>
          </ul>
        </li>
        <li class="col-sm-4">
          その他、インフラや開発ツール
          <ul>
            <li v-for="other in skillSet.other" :key="other">
              {{ other }}
            </li>
          </ul>
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
