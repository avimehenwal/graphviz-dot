<template>
  <div>
    <DotLanguage
      code="digraph {
        node [fontsize=24, colorscheme=set312, style=filled]
        a [fillcolor=1]
        b [fillcolor=2]
        c [fillcolor=3]
        a -> b -> c
      }"
    />
  </div>
</template>

<script>
import DotLanguage from './components/DotLanguage.vue';

export default {
  name: 'home',
  components: {
    DotLanguage,
  },

};
</script>
