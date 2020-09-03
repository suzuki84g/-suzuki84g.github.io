<template>
  <div class="skill row">
    <h2 class="col-12">
      Skill
    </h2>
    <div v-for="skill in skills" :key="skill" class="col-12">
      <p>{{ skill.language }} / Level {{ skill.level }}</p>
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
