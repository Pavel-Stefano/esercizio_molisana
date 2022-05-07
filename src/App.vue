<template>
  <div id="app">
    <app-header />
    <main>
      <app-products />
    </main>
    <app-footer />
  </div>
 
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppProducts from './components/AppProducts.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  name: 'App',
  components: {
    AppHeader,
    AppProducts,
    AppFooter
  },
  data(){ 
    return {
     
    
    }
  },
  methods:{

  }
}
</script>

<style lang="scss">
@import "./style/vars";
@import "./style/generals";
@import "./style/utilities";

h1,
h2,
h3,
h4,
h5,
h6 {
    color: $primary;
}
</style>
