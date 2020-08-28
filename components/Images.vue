<template>
  <div class="image">
    <h2>Activity</h2>
    <div v-for="item in items" :key="item">
      <h3>{{ item.title }}</h3>
      <figure v-for="image in item.images" :key="image">
        <img :src="image.imgSrc">
        <figcaption>{{ image.caption }}</figcaption>
      </figure>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'ゲーム',
          images: [
            {
              imgSrc: require('@/assets/image/image0.jpg'),
              caption: '写真右 2020年2月 スプラトゥーン甲子園関東地区大会'
            }
          ]
        },
        {
          title: '料理',
          images: [
            {
              imgSrc: require('@/assets/image/IMG_1805.jpg'),
              caption: 'カレーの材料'
            },
            {
              imgSrc: require('@/assets/image/IMG_8155.jpg'),
              caption: '煮込んだあとの様子です'
            },
            {
              imgSrc: require('@/assets/image/IMG_2581.jpg'),
              caption: '初期ロット'
            },
            {
              imgSrc: require('@/assets/image/IMG_2781.JPG'),
              caption: '改良型'
            },
            {
              imgSrc: require('@/assets/image/IMG_2852.jpg'),
              caption: '家庭向け'
            },
            {
              imgSrc: require('@/assets/image/IMG_7053.jpg'),
              caption: '製麺機を見つけたので体験する'
            },
            {
              imgSrc: require('@/assets/image/IMG_2753.jpg'),
              caption: '良い感じにミートソースを作る'
            },
            {
              imgSrc: require('@/assets/image/IMG_2755.jpg'),
              caption: '見た目だけはよく出来たけど肝心の麺が大変微妙だった'
            }
          ]
        }
      ]
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
