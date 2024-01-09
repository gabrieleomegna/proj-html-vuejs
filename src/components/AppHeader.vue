<script>
    import ButtonComponent from './smallComponents/ButtonComponent.vue';
    export default {
        components : {
    ButtonComponent,
},
        props : {
            phoneNumber : {
                type: String,
                required: true
            },
            menuItems : {
                type: Array,
                required: true
            }
        }
    }
</script>

<template>
    <header>
        <!-- ? Qua secondo me l'header è diviso in 4 parti, che potrebbero diventare componenti -->
        <section class="call-section">
            <!-- Questa sezione è molto simile all'ultima del footer, ma con alcune parti in meno
                 e, soprattutto, le due 'parti' in cui è divisa sono in linea, MENTRE NEL FOOTER SONO IN COLONNA  -->
            <!-- ? dimensione comune -->
            <div class="container">
                <section id="number-to-call"> <!-- Number to call -->
                    <i class="fa-solid fa-phone-flip"></i>
                    <span>Call us for a Free Quote: {{ phoneNumber }}</span>
                </section>
                <section> <!-- Brands symbol -->
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-youtube"></i>
                </section>
            </div>
        </section>
        <div id="same-bg">
            <nav class="container">
                <!-- Questa sezione sarà popolata con le voci di menu CHE ARRIVERANNO DIRETTAMENTE DALL'APP VUE TRAMITE PROPS-->
                <section>
                    <span>Logo</span>
                </section>
                <section id="menu-items">
                    <span v-for="singleItem in menuItems">{{ singleItem.label }}</span>
                    <ButtonComponent :size="'small'"
                                     :content="'Free Quote'" />
                </section>
            </nav>
            <section class="jumbotron">
                <!-- Questa sezione per me è palesemente un jumbotron -->
                <!-- ? ATTENZIONE jumbotron e navbar hanno lo sfondo in comune,
                     ? perciò li ho messi all'interno di un div unico -->
    
            </section>
        </div>
        <section id="blue-free-quote">

        </section>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    .call-section {
        background-color: $hdr-ftr-bg-color;
        color: white;
        padding: .7rem 0;
        .container {
            @include flex (row, space-between, center);
            * > * {
                font-size: .7rem;
                margin-left: 1rem;
            }
        }
    }

    nav.container {
        @include flex(row, space-between, center)
    }
</style>