<template>
    <main>
        <!-- ? Qua ci sono 5 sezioni, per cui farò 5 diversi componenti -->
        <AppAward/>

        <ServiceSolution/> <!-- Qua ci sono 3 diverse card, a cui passerò tramite props
                                le immagini, il titolo, la descrizione. Mentre i bottoni sono tutti e 3 UGUALI -->
                           <!-- ? dimensione comune -->
        
        <MoveWithEase/>   <!-- ? dimensione comune -->
                          <!-- Questa sezione ha un immagine come bg -->
        
        <AppTestimonials/> <!-- Qua c'è un'immagine come sfondo ma che si vede molto poco (capire se si tratta di opacità) 
                                Inoltre qua ho altre 3 card, DIVERSE da quelle in ServiceSolution, che andrò a popolare con immagine, nome e descrizione-->
                           <!--? dimensione comune -->

        <RequestFreeQuote/>
    </main>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
    
</style>