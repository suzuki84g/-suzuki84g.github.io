<template>
  <v-row class="link">
    <v-col cols="12" class="row-title">
      Link
    </v-col>
    <v-col cols="3">
      <a href="https://github.com/suzuki84g/" class="col-3">
        <img :src="icon.github" class="icon">
      </a>
    </v-col>
    <v-col cols="3">
      <a href="https://qiita.com/suzuki_cs" class="col-3">
        <img :src="icon.qiita" class="icon">
      </a>
    </v-col>
    <v-col cols="3">
      <a href="https://docs.google.com/forms/d/e/1FAIpQLSfHFyNjfbH8tWLs9-GVh9Ax3QKBpFs6OwdVaAXmdTn183q7ew/viewform?usp=sf_link" class="col-3">
        <img :src="icon.gmail" class="icon">
      </a>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      icon: {
        github: require('@/assets/image/logo/GitHub-Mark-120px-plus.png'),
        qiita: require('@/assets/image/logo/qiita.png'),
        gmail: require('@/assets/image/logo/googlemail-128.png')
      }
    }
  }
}
</script>

<style lang="scss">
.icon {
  width: 60px;
  height: auto;
}
</style>
