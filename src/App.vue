<template>
  <div>
    <script src="https://unpkg.com/@hpcc-js/wasm/dist/index.min.js" type="javascript/worker"></script>
    <GraphvizViewer />
  </div>
</template>

<script>
import GraphvizViewer from './components/GraphvizViewer.vue';

export default {
  name: 'home',
  components: {
    GraphvizViewer,
  },

};
</script>
