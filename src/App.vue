<template>
  <div id="app">
    <div class="main-layout">
      <div class="col">
        <sidebar />
      </div>
      <div class="col">
        <topbar />  
        <layout-data />  
      </div> 
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import topbar from './components/Topbar.vue'
import sidebar from './components/Sidebar.vue'
import layoutData from './components/Content.vue'
export default {
  name: 'app',
  components: {
    // HelloWorld
    topbar,
    sidebar,
    'layout-data': layoutData
    
  }
}
</script>

<style lang="scss">
#app {
  @import url('https://fonts.googleapis.com/css?family=Open+Sans:300,400,700');
  @import '@/assets/styles/_vars.scss';
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  // margin-top: 60px;
  // margin: 0;
}
* {
    margin: 0;
    padding: 0;
  }

.main-layout {
  display: flex;
  .col:nth-child(1) {
    flex: 1;
  }
  .col:nth-child(2) {
    flex: 6;
  }
}
</style>
