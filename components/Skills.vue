<template>
  <div>
    <div v-for="skill in skills" :key="skill">
      <div class="skill">
        <p>{{ skill.language }}</p>
        <p>{{ skill.level }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      skills: [
        {
          language: 'html',
          level: '3'
        },
        {
          language: 'css/sass',
          level: '4'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
