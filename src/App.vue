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
          companyTelephoneNumber: '1.800.555.6789',
          navMenuItems: [
            {
              label: 'Home',
              link : ''
            },
            {
              label: 'Rates',
              link: ''
            },
            {
              label: 'Testimonials',
              link: ''
            },
            {
              label: 'FAQ',
              link: ''
            },
            {
              label: 'Blog',
              link: ''
            },
            {
              label: 'Contact',
              link: ''
            }
          ],
          ftrMenuItems: [
            {
              label: 'Home',
              link : ''
            },
            {
              label: 'Rates',
              link: ''
            },
            {
              label: 'Testimonials',
              link: ''
            },
            {
              label: 'Blog',
              link: ''
            },
            {
              label: 'Free Quote',
              link: ''
            }
          ],
          ftrRecentPosts: [
            {
              string: 'Heading Out To College?',
              link : ''
            },
            {
              string: 'Moving Your Business?',
              link: ''
            },
            {
              string: 'Outstanding Quality',
              link: ''
            },
            {
              string: 'Cost of Moving',
              link: ''
            },
            {
              string: 'Best Moving Tips',
              link: ''
            }
          ],
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
    <AppHeader :phoneNumber = "companyTelephoneNumber"
               :menuItems = "navMenuItems"/>
    <AppMain/>
    <AppFooter :menuItems="ftrMenuItems"
               :recentPostItems="ftrRecentPosts"/>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>
