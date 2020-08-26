<template>
  <div class="profile">
    <h2>Plofile</h2>
    <p>{{ nameKanzi }} / {{ nameAlphabet }}</p>
    <span>{{ myBirthday.year }}年{{ myBirthday.month }}月{{ myBirthday.day }}日</span>
    <span>年齢 {{ age }}</span>
    <figure class="photo">
      <img :src="recentPhotograph.imgSrc" alt="近影">
      <figcaption>{{ recentPhotograph.caption }}</figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  data () {
    return {
      nameKanzi: '鈴木 優紀',
      nameAlphabet: 'SUZUKI Yuki',
      myBirthday: {
        year: 1988,
        month: 10,
        day: 27
      },
      age: {},
      calcDate: {
        birthday: {},
        today: {}
      },
      recentPhotograph: {
        imgSrc: require('@/assets/image/image0.jpg'),
        caption: '写真右 2020年2月 スプラトゥーン甲子園関東地区大会'
      }
    }
  },
  mounted () {
    this.calcAge()
  },
  methods: {
    dateTypeCasting (date, push) {
      push.y = date.getFullYear().toString().padStart(4, '0')
      push.m = (date.getMonth() + 1).toString().padStart(2, '0')
      push.d = date.getDate().toString().padStart(2, '0')
    },
    calcAge () {
      const birthDate = new Date(this.myBirthday.year, this.myBirthday.month - 1, this.myBirthday.day) // 誕生日のDateインスタンス化
      const today = new Date() // 今日の日付を取得
      const inData = this.calcDate
      this.dateTypeCasting(birthDate, inData.birthday) // 引数渡して文字列に分解する
      this.dateTypeCasting(today, inData.today) // 引数渡して文字列に分解する
      this.age = Math.floor((Number(inData.today.y + inData.today.m + inData.today.d) - Number(inData.birthday.y + inData.birthday.m + inData.birthday.d)) / 10000) // 誕生日を計算
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
