<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    import AppFooter from './components/AppFooter.vue';

    export default {
      components: {
        AppHeader,
        AppMain,
        AppFooter
      },
      data() {
        return {
          companyTelephoneNumber: '1.800.555.6789'
        }
      }
    }
</script>
<!-- ? ATTENZIONE: in tutto il layout abbiamo una dimensione di container uguale in molte sezioni:
     ? prime due sezioni dell'header;
     ? tutte le sezioni del main, eccetto la prima e l'ultima; 
     ? la prima sezione del footer
     ? per le altre posso o lasciarle nel container e aggiustarlo con il padding,
     ? oppure fare io manualmente il container-->
<!-- Tutto ciò dando per scontato di usare bootstrap -->


<template>
    <AppHeader :phoneNumber = "companyTelephoneNumber"/>
    <AppMain/>
    <AppFooter/>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>
