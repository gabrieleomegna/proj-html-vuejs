<template>
    <section id="service-solution">
        <p>We are a professional</p>
        <h2>Full-Service solution</h2>
        <div class="container">
            <ServiceCard/>
        </div>
    </section>
</template>
<script>
import ServiceCard from './ServiceCard.vue';
export default {
    components: {
        ServiceCard
    }
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/mixins' as *;
@use '../../styles/partials/variables' as *;

section#service-solution {
    p,
    h2 {
        text-align: center;
    };
    h2 {
        font-weight: 900;
    };
    .container {
        @include flex (row, space-between, center)
    }
}
</style>