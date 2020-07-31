Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@Ligiki1 
lisaschulzke
/
hfg_exhibition
1
0
0
Code
Issues
Pull requests
3
Actions
Projects
Wiki
Security
Insights
hfg_exhibition/src/App.vue
@lisaschulzke
lisaschulzke fixing bugs
Latest commit a7d1126 1 hour ago
 History
 1 contributor
43 lines (37 sloc)  1010 Bytes
  
<template>
  <div id="app">
    <Layout streamUrl="http://hal.hfg.design:50005/live-21080.mjpg">

      <template v-slot:videocomponent></template>
      <template v-slot:controlcomponent>
        <Interface></Interface>
      </template>
      <template v-slot:queuecomponent>
        <SimpleQueueComponent></SimpleQueueComponent>
        <!-- <h1>BOTTOM_RIGHT</h1> -->
      </template>

    </Layout>
  </div>
</template>

<script>
  import Interface from './components/interface.vue';
  import Layout from './submodules/base_layout/src/components/interface.vue'
  import SimpleQueueComponent from './components/SimpleQueueComponent.vue'
  export default {
    name: 'App',
    components: {
      Interface,
      Layout,
      SimpleQueueComponent,
    },
  };
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
