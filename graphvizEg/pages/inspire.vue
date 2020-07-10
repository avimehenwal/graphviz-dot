<template>
  <v-layout>
    <!-- <nuxt-content :document="chart" /> -->
    <!-- {{ chart }} -->
    <v-img src="/svg/graph1.svg" />

    <v-flex class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  // async asyncData ({ $content }) {
  //   const chart = await $content('graph1.dot').fetch()
  //   return { chart }
  // }
}
</script>
