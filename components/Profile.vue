<template>
  <section>
    <div class="title">
      <h2>About</h2>
    </div>
    <div class="profile-container">
      <div class="avatar">
        <img src="/favicon_package_v0.16/android-chrome-512x512.png" alt="self-icon">
      </div>
      <div class="introduction">
        <div class="name-box">
          <h3>{{ nameKanzi }} / {{ nameAlphabet }}</h3>
        </div>
        <div class="base-status">
          <div class="text-box">
            <p>Webエンジニア / 主夫</p>
            <p>{{ myBirthday.year }}/{{ myBirthday.month }}/{{ myBirthday.day }} ({{ age }})</p>
            <p>{{ mail }}</p>
          </div>
          <div class="pokedex">
            <p>{{ profileSentence1 }}</p>
            <p>{{ profileSentence2 }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
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
      profileSentence1: 'ネットワークSI出身のWebエンジニア。',
      profileSentence2: '特性を活かした爆発力がある為、こだわりアイテムとの相性が良い。'
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
.profile-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: auto;
  @media screen and (max-width: 414px) {
    // SPモード
    flex-direction: column;
  }
  >div {
    margin: 0 2em;
  }
  .avatar {
    width: 20%;
    img {
      border-radius: 50%;
    }
  }
  .introduction {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    .base-status {
      width: auto;
      align-self: start;
      margin-bottom: 1rem;
      .text-box,
      .pokedex {
        margin-left: 1rem;
        margin-bottom: 0.5rem;
      }
    }
  }
}
</style>
