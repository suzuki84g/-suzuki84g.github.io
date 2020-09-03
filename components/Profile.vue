<template>
  <div class="profile row">
    <h2 class="col-12">
      Plofile
    </h2>
    <img class="col-sm-6" src="/favicon_package_v0.16/android-chrome-512x512.png" alt="image">
    <div class="col-sm-6">
      <p>{{ nameKanzi }} / {{ nameAlphabet }}</p>
      <p>{{ myBirthday.year }}年{{ myBirthday.month }}月{{ myBirthday.day }}日</p>
      <p>年齢 {{ age }}</p>
      <p>{{ profileSentence.message }}</p>
    </div>
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
      mail: 'suzuki.84g@gmail.com',
      age: {},
      calcDate: {
        birthday: {},
        today: {}
      },
      profileSentence: require('@/assets/json/profileSentence.json')
    }
  },
  computed: {
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
</style>
