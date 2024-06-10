<script setup>

  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';


 

</script>

<template>
  <HeaderComponent></HeaderComponent>
  <MainComponent></MainComponent>
  <FooterComponent/>
</template>

<style lang="scss">

@use './styles/general.scss';
@use './styles/partials/variables';
@use './styles/partials/mixin'

</style>
