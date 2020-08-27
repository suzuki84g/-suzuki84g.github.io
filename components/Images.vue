<template>
  <div class="image">
    <figure>
      <img :src="recentPhotograph.imgSrc" alt="近影">
      <figcaption>{{ recentPhotograph.caption }}</figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  data () {
    return {
      recentPhotograph: {
        imgSrc: require('@/assets/image/image0.jpg'),
        caption: '写真右 2020年2月 スプラトゥーン甲子園関東地区大会'
      }
    }
  }
}
</script>

<style lang="scss">
img {
  width: 100%;
  height: auto;
}
</style>
