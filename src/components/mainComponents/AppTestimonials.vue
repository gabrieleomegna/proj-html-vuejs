<template>
    <section id="testimonials">
        <p>Happy Customers</p>
        <h2>Testimonials</h2>
        <div class="container">
            <TestimonialCard v-for="singleTestimonial in testimonials" :singleTestimonial="singleTestimonial"/>
        </div>
        <div class="btn-container">
            <ButtonComponent :size="'small'"
                             :content="'Read More Testimonials'"/>
        </div>
    </section>
</template>
<script>
import TestimonialCard from './cards/TestimonialCard.vue';
import ButtonComponent from '../smallComponents/ButtonComponent.vue';
export default {
    components: {
        TestimonialCard,
        ButtonComponent
    },
    data() {
        return {
            testimonials : [
                {
                    name: 'John Doe',
                    pathImage: 'avada-movers-johndoe-final.jpg',
                    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores repellat, mollitia obcaecati ad sit soluta dignissimos saepe ea qui dolorum ducimus. Tempora dignissimos dolorum eligendi?"',
                },
                {
                    name: 'Jane Doe',
                    pathImage: 'avada-movers-janedoe-final.jpg',
                    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores repellat, mollitia obcaecati ad sit soluta dignissimos saepe ea qui dolorum ducimus. Tempora dignissimos dolorum eligendi?"',
                },
                {
                    name: 'John Smith',
                    pathImage: 'avada-movers-johnsmith-final.jpg',
                    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores repellat, mollitia obcaecati ad sit soluta dignissimos saepe ea qui dolorum ducimus. Tempora dignissimos dolorum eligendi?"',
                },
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/mixins' as *;
@use '../../styles/partials/variables' as *;

section#testimonials {
    padding: 7rem 0;
    background-image: url('../../assets/img/avada-movers-testimonial-background.jpg');
    background-size: cover;
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
        @include flex (row, space-between, center);
        margin-bottom: 4rem;
    }
    .btn-container {
        @include flex (row,center,center)
    }
}
</style>