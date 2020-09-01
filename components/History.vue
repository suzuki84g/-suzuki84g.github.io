<template>
  <div class="history">
    <h2>Timeline</h2>
    <table>
      <tbody>
        <tr v-for="history in history" :key="history.year">
          <th>{{ history.year }}年 {{ history.month }}</th>
          <td>{{ history.value }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      history: [
        { year: 2011, month: '春', value: '大学を卒業し、SIerへのSES事業を行う都内の企業に就職。ネットワーク機器、サーバの運用保守を中心に、金融機関本社の移転PJなど、様々な案件を経験する。' },
        { year: 2017, month: '夏', value: 'エンジニアとしての技術が全く身についていない事に危機感を覚え、ECシステムを中心に扱う同業他社に転職。大手通信会社系のSIerに常駐し、Linux/Windowsで稼働するシステム全般の運用保守、開発提案業務を行う。' },
        { year: 2018, month: '夏', value: '結局何も変えられなかった事に気付き、退職する。家内からの指摘から通院したところ、ADHDと鬱の診断が下る。各種手当を受け取りつつ、専業主夫生活を開始する。' },
        { year: 2019, month: '通年', value: '無職の限りを尽くす傍ら、Web系の学習を始める。フリーランス、リモート勤務の友人と仲間内のもくもく会を都内某所のコワーキングスペースで開催。カレーを提供する事でgitやチーム開発など、独学の難しい技術を教わり、また社会との接点を維持する事に成功。' },
        { year: 2020, month: '年明け', value: '失業手当への切り替えでハローワークに行った際、就労移行支援制度の存在を知る。「職業：Webエンジニア」への道が拓ける事業所への通所を開始。' },
        { year: 2020, month: '夏', value: '事業所内での案件に参画しある程度は技術を修めたと判断、失業手当が差し迫る為、就職活動を開始。退職当時にコロナ不況は読めなかった…。' },
        { year: 2020, month: '秋', value: 'To be continued △▽△' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
