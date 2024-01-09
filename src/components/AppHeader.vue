<template>
    <header>
        <!-- ? Qua secondo me l'header è diviso in 4 parti, che potrebbero diventare componenti -->
        <section class="call-section container">
            <!-- Questa sezione è molto simile all'ultima del footer, ma con alcune parti in meno
                 e, soprattutto, le due 'parti' in cui è divisa sono in linea, MENTRE NEL FOOTER SONO IN COLONNA  -->
            <!-- ? dimensione comune -->
            <div> <!-- Number to call -->
                <p>Call us for a Free Quote: {{ phoneNumber }}</p>
            </div>
        </section>
        <div id="same-bg">
            <nav class="navbar">
                <!-- Questa sezione sarà popolata con le voci di menu CHE ARRIVERANNO DIRETTAMENTE DALL'APP VUE TRAMITE PROPS-->
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
<script>
    export default {
        props : [
            'phoneNumber'
        ]
    }
</script>
<style lang="scss" scoped>
    
</style>