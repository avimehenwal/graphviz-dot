<template>
  <div>
    <script src="https://unpkg.com/@hpcc-js/wasm/dist/index.min.js" type="javascript/worker" />
    <h3>from Component</h3>
    <div id="graph" />
  </div>
</template>

<script>
import * as d3 from 'd3'
import 'd3-graphviz'

export default {
  props: {
    code: {
      type: String,
      default: 'digraph {a -> b}'
    }
  },
  mounted () {
    d3.select('#graph').graphviz('#graph').renderDot(this.code)
  }
}
</script>