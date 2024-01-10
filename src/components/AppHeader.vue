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
        },
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
        <div id="same-bg-img">
            <nav class="container">
                <!-- Questa sezione sarà popolata con le voci di menu CHE ARRIVERANNO DIRETTAMENTE DALL'APP VUE TRAMITE PROPS-->
                <section id="logo">
                    <img src="../assets/img/avada-movers-logo.png" alt="Company logo">
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
                <div id="jmbt-block">
                    <p>Moving without the hassle</p>
                    <h1>We make it simple</h1>
                    <p>Professional service with quality and customer satisfaction</p>
                </div>
            </section>
        </div>
        <section id="blue-free-quote">
            <p><i class="fa-regular fa-paper-plane"></i> <span>Get a free quote online now</span></p>
        </section>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    /***  Small section green ****/
    .call-section {
        background-color: $hdr-ftr-bg-color;
        color: white;
        padding: .7rem 0;
        .container {
            @include flex (row, space-between, center);
            * > * {
                font-size: .65rem;
                margin-left: 1rem;
            }
        }
    }
    
    /***  NAVBAR ****/
    nav.container {
        @include flex(row, space-between, center);
        padding: .7rem 0 .7rem 1rem;
        section#menu-items > * {
            margin-left: 2rem;
        };
        section#menu-items > span {
            font-size: .7rem;
            font-weight: 900;
        }
        section#logo img{
            width: 135px;
        }
    }

    /***  JUMBOTRON ****/
    .jumbotron {
        height: 500px;
        @include flex(row, center, center);
        #jmbt-block > * {
            margin-bottom: .5rem;
            text-align: center;
            text-transform: uppercase;
            font-weight: 900;
        };
        #jmbt-block p:first-child,
        #jmbt-block p:nth-child(3) {
            color: rgb(124, 120, 120);
            font-size: .67rem;
        }
        #jmbt-block h1{
            font-size: 2.6rem;
        }
    }
    /* Bg image */
    div#same-bg-img{
        background-image: url('../assets/img/avada-movers-homeherobackground-final.jpg');
        background-position: top;
        background-size: 1800px;
        background-repeat: no-repeat;
    }

    /* Blue free quote section */
    section#blue-free-quote{
        padding: 2rem;
        background-color: $section-free-quote-bg;
        p {
            text-align: center;
            text-transform: uppercase;
            color: white;
            font-size: .78rem;
            span {
                margin-left: .4rem;
            }
        }
    }

</style>