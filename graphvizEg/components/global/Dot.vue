<template>
  <v-container class="justify-center">
    <script type="javascript/worker" src="https://unpkg.com/@hpcc-js/wasm/dist/index.min.js" />
    <!-- <script type="javascript/worker" src="../../node_modules/@hpcc-js/wasm/dist/index.min.js" /> -->
    <h4>{{ identifier }}</h4>
    <div :id="id" style="text-align: center;" />
  </v-container>
</template>

<script>
import * as d3 from 'd3'
import 'd3-graphviz'
// import 'hpcc-js/wasm/dist/index.min.js'

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
  computed: {
    identifier () {
      return ('#' + this.id)
    }
  },
  mounted () {
    const t = d3.transition()
      .duration(4000)
      .ease(d3.easeLinear)

    d3.select(this.identifier)
      .graphviz(this.identifier)
      .width('80%')
      .engine('neato')
      .scale(3)
      // .graphviz.fade(enable)
      .transition(t)
      // .attributer(this.attributerfn(d))
      // .style('background-color', 'red')
      // .style('fill', 'red')
      .renderDot(this.code)
      .on('end', this.interactive)
  },
  methods: {
    transition1 () {
      return d3.transition()
        .delay(100)
        .duration(1000)
    },
    attributerfn (d) {
      if (d.tag == "ellipse") {
        d3.select(this)
          .attr("fill", "yellow");
        d.attributes.fill = "red";
      }
    }
    // interactive () {
    //   let nodes = d3.selectAll('.node,.edge')
    //   nodes.on("click", function () {
    //     removeDrawnNode()
    //   })
    // }
  }
}
</script>
