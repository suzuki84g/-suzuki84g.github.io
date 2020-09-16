<template>
  <div class="link-components">
    <div v-for="service in sns" :key="service.name" class="sns-item">
      <a :href="service.url">
        <img :src="service.icon" alt="service-icon" class="icon">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      sns: [
        {
          name: 'GitHub',
          url: 'https://github.com/suzuki84g/',
          icon: require('@/assets/image/logo/GitHub-Mark-120px-plus.png')
        },
        {
          name: 'Qiita',
          url: 'https://qiita.com/suzuki_cs',
          icon: require('@/assets/image/logo/qiita.png')
        },
        {
          name: 'mailform',
          url: 'https://docs.google.com/forms/d/e/1FAIpQLSfHFyNjfbH8tWLs9-GVh9Ax3QKBpFs6OwdVaAXmdTn183q7ew/viewform?usp=sf_link',
          icon: require('@/assets/image/logo/googlemail-128.png')
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.link-components {
  display: flex;
  flex-direction: row;
  justify-content: center;
  .sns-item {
    margin: 0 1rem;
    .icon {
      width: 60px;
      height: auto;
    }
  }
}
</style>
