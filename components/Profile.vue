<template>
  <div class="content">
    <div class="title">
      <h2>About</h2>
    </div>
    <div class="mainContainer">
      <div class="avatar">
        <img src="/favicon_package_v0.16/android-chrome-512x512.png" alt="self-icon">
      </div>
      <div class="introduction">
        <div class="base-status">
          <h3>{{ nameKanzi }} / {{ nameAlphabet }}</h3>
          <p>Webエンジニア / 主夫</p>
          <p>{{ myBirthday.year }}/{{ myBirthday.month }}/{{ myBirthday.day }} ({{ age }})</p>
          <p>{{ mail }}</p>
        </div>
        <div class="sns-link">
          <Link />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Link from '~/components/Link'

export default {
  data () {
    return {
      components: [
        Link
      ],
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
.mainContainer {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: auto;
  >div {
    margin: 0 2em;
  }
  .avatar {
    width: 30%;
    img {
      border-radius: 50%;
    }
  }
  .introduction {
    display: flex;
    flex-direction: column;
    justify-content: center;
    .base-status {
      width: auto;
      align-self: center;
    }
  }
}
</style>
