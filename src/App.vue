<script>
  import AppHeader from "./components/AppHeader.vue"
  import AppFooter from "./components/AppFooter.vue"
  import AppMain from "./components/AppMain.vue"
  export default {    
    components:{
      AppHeader,
      AppFooter,
      AppMain
    }
  }
</script>

<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
  </div>
</template>

<style lang="scss">
  @use "./styles/general.scss" as *;
</style>