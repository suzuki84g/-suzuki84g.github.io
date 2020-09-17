<template>
  <section>
    <div class="title">
      <h2>Skill</h2>
    </div>
    <div class="skill-container">
      <div v-for="skill in skillSet" :key="skill.field" class="skill">
        <div class="name-box">
          <h3>{{ skill.field }}</h3>
        </div>
        <ul>
          <li v-for="ability in skill.abilitys" :key="ability" class="abilitys">
            {{ ability }}
          </li>
          <p class="comment">
            {{ skill.comment }}
          </p>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      skillSet: [
        {
          field: 'フロントエンド',
          abilitys: ['HTML5', 'CSS3', 'sass', 'JavaScript', 'Bootstrap', 'Vue.js', 'Nuxt.js', 'Vuetify'],
          comment: 'モダンなWebサイトの理解、フレームワークの使用、REST APIの利用など。'
        },
        {
          field: 'バックエンド',
          abilitys: ['Linux', 'WindowsServer', 'Python', 'Node.js', 'MySQL', 'AWS'],
          comment: 'CLIの操作、Webアプリケーションの運用、DBの管理、AWS EC2の構築、シンプルなPythonプログラムの作成。'
        },
        {
          field: 'その他',
          abilitys: ['git', 'GitHub', 'docker', 'Vagrant', 'Heroku', 'PMO', 'オンプレミス環境の物理作業'],
          comment: '開発コードの管理や仮想環境の構築。プロジェクト進行管理など。'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.skill-container {
  display: flex;
  flex-direction: column;
  align-items: start;
  .skill {
    margin-bottom: 1rem;
  }
  ul {
    margin: 0 1rem 1rem;
    .comment {
      font-size: small;
    }
  }
  li {
    display: inline;
    font-weight: bold;
  }
}
</style>
