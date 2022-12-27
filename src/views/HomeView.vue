<template>
  <div class="home">

    <TopView></TopView>
    <wel-come></wel-come>

    <button @click="ToAbout">跳转</button>
  </div>
</template>

<script>
  // import WelCome from '../components/WelCome'
export default {
  name: 'HomeView',
  components: {
    TopView:()=>import('../components/TopView'),
    WelCome:()=>import('../components/WelCome')
      // WelCome
  },
  methods:{
    ToAbout(){
      this.$router.push({path:'/about'})
    },
  },
};
</script>
<style scoped>

</style>
