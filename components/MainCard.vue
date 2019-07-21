<template>
  <section>
    <main>
      <news-card-a class="card" />
      <news-card-b class="card" />
      <news-card-c class="card" />
      <news-card-d class="card" />
      <news-card-e class="card" />
      <news-card-f class="card" />
      <news-card-g class="card" />
      <news-card-h class="card" />
      <news-card-i class="card" />
      <news-card-j class="card" />
      <news-card-k class="card" />
    </main>
  </section>
</template>

<script>
import NewsCardA from './NewsCardA.vue'
import NewsCardB from './NewsCardB.vue'
import NewsCardC from './NewsCardC.vue'
import NewsCardD from './NewsCardD.vue'
import NewsCardE from './NewsCardE.vue'
import NewsCardF from './NewsCardF.vue'
import NewsCardG from './NewsCardG.vue'
import NewsCardH from './NewsCardH.vue'
import NewsCardI from './NewsCardI.vue'
import NewsCardJ from './NewsCardJ.vue'
import NewsCardK from './NewsCardK.vue'

export default {
  components: {
    NewsCardA,
    NewsCardB,
    NewsCardC,
    NewsCardD,
    NewsCardE,
    NewsCardF,
    NewsCardG,
    NewsCardH,
    NewsCardI,
    NewsCardJ,
    NewsCardK,
  },
}
</script>

<style lang="scss" scoped>
section {
  display: grid;
  overflow: hidden;
  margin-top: 11.25rem;
  main {
    display: grid;
    justify-content: center;
    padding: 30px;
    /* min-width: 1000px; */
    max-width: 1170px;
    width: 1170px;

    justify-self: center;
    grid-template-columns: repeat(4, 1fr);
    grid-template-areas:
      'a b b c'
      'a d e f'
      'g g h i'
      'j j j k';
    grid-gap: 30px;
    .card {
      border-radius: 6px;
      background-color: white;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.05);
    }
  }
}
</style>
