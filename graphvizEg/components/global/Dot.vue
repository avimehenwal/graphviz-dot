<template>
  <div>
    <script type="javascript/worker" src="https://unpkg.com/@hpcc-js/wasm/dist/index.min.js" />
    <h4>{{ identifier }}</h4>
    <div :id="id" />
  </div>
</template>

<script>
import * as d3 from 'd3'
import 'd3-graphviz'
// import '@hpcc-js/wasm'

export default {
  props: {
    code: {
      type: String,
      default: 'digraph {a -> b}'
    },
    id: {
      type: String,
      default: 'graph'
    }
  },
  mounted () {
    d3.select(this.identifier).graphviz(this.identifier).renderDot(this.code)
  },
  computed: {
    identifier () {
      return ('#' + this.id)
    }
  }
}
</script>
