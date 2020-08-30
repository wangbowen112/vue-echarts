<template>
  <div id="app">
    <datasetSimple0 />
    <lineSimple />
    <mixLineBar />
    <pieLegend />
  </div>
</template>
<script>
  import datasetSimple0
    from "./components/datasetSimple0";
  import lineSimple
    from "./components/lineSimple";
  import mixLineBar
    from "./components/mixLineBar";
  import pieLegend from "./components/pieLegend";

  export default {
    components:{
      datasetSimple0,
      lineSimple,
      mixLineBar,
      pieLegend
    }
  }

</script>
<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
