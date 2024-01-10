<template>
    <section id="testimonials">
        <p>Happy Customers</p>
        <h2>Testimonials</h2>
        <div class="container">
            <TestimonialCard/>
        </div>
    </section>
</template>
<script>
import TestimonialCard from './cards/TestimonialCard.vue';
export default {
    components: {
        TestimonialCard
    }
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/mixins' as *;
@use '../../styles/partials/variables' as *;

section#testimonials {
    padding: 6.5rem 0;
    p,
    h2 {
        text-align: center;
    };
    p{
        color: rgb(170, 170, 170);
        font-size: .8rem;
        font-weight: 800;
        text-transform: uppercase;
        margin-bottom: .5rem;
    }
    h2 {
        font-size: 2rem;
        font-weight: 900;
        color: $titles-color;
        margin-bottom: 2.5rem;
    };
    .container {
        @include flex (row, space-between, center)
    }
}
</style>