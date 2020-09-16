<template>
  <div class="content">
    <div class="title">
      <h2>Skill</h2>
    </div>
    <div v-for="skill in skillSet" :key="skill.field" class="skill">
      <div class="name-box">
        <h3>{{ skill.field }}</h3>
      </div>
      <ul>
        <li v-for="ability in skill.abilitys" :key="ability">
          {{ ability }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      skillSet: [
        {
          field: 'フロントエンド',
          abilitys: ['html', 'css/sass', 'javascript', 'Bootstrap', 'Vue.js', 'Nuxt.js', 'Vuetify']
        },
        {
          field: 'バックエンド',
          abilitys: ['Linux', 'WindowsServer', 'Python', 'Node.js', 'MySQL']
        },
        {
          field: 'その他',
          abilitys: ['git', 'GitHub', 'docker', 'Vagrant', 'AWS', 'Heroku', 'PMO', 'オンプレミス環境の物理作業']
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.skillsContainer {
  display: flex;
  flex-direction: column;
  align-items: start;
}
</style>
