<template>
  <div class="profile">
    <h2>Name</h2>
    <span>{{ nameKanzi }}</span>
    <span>{{ nameAlphabet }}</span>
    <span>{{ birthday }}</span>
    <figure class="photo">
      <img src="~assets/image/photo.png" alt="近影">
      <figcaption>写真右 2020年2月 スプラトゥーン甲子園関東地区大会</figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  data () {
    return {
      nameKanzi: '鈴木 優紀',
      nameAlphabet: 'SUZUKI Yuki',
      birthday: 19881027,
      recentPhotograph: {
        picture: 'hoge',
        caption: 'fuga'
      }
    }
  }
}
</script>

<style lang="scss">
</style>
