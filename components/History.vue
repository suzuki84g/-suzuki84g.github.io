<template>
  <div class="history">
    <h2>Timeline</h2>
    <table>
      <tbody>
        <tr v-for="history in history" :key="history.year">
          <td>{{ history.year }}年 {{ history.value }}</td>
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
        { year: 2013, value: '二松学舎大学 国際政治経済学部 卒業' },
        { year: 2013, value: '入社' },
        { year: 2017, value: '転職' },
        { year: 2018, value: '退職' },
        { year: 2020, value: '就職活動' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
