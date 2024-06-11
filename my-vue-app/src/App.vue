<script >

  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';

  export default {
    data(){
      return{
        message: "benvenuti"
      }
    }, 
    
    components:{
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
 
  }
 

</script>

<template>
  <HeaderComponent></HeaderComponent>
  <MainComponent :messaggio="message"></MainComponent>
  <FooterComponent/>
</template>

<style lang="scss">

@use './styles/general.scss';
@use './styles/partials/variables';
@use './styles/partials/mixin'

</style>
