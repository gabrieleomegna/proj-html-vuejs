<template>
    <section id="service-solution">
        <p>We are a professional</p>
        <h2>Full-Service solution</h2>
        <div class="container">
            <ServiceCard v-for="singleSolution in serviceSolutions" :singleSolution="singleSolution"/>
        </div>
    </section>
</template>
<script>
import ServiceCard from './cards/ServiceCard.vue';
export default {
    components: {
        ServiceCard
    },
    data() {
        return {
            serviceSolutions: [
                {
                    pathImage: 'avada-movers-serviceonephoto-final-600x383.jpg',
                    title: 'Two Man Teams',
                    description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus, labore commodi? Recusandae eligendi placeat a omnis. Non praesentium nihil mollitia cumque repellat, at',
                },
                {
                    pathImage: 'avada-movers-servicetwophoto-final.jpg',
                    title: 'We Do All The Lifting',
                    description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus, labore commodi? Recusandae eligendi placeat a omnis. Non praesentium nihil mollitia cumque repellat, at',
                },
                {
                    pathImage: 'avada-movers-servicethreephoto-final.jpg',
                    title: 'Coast To Coast',
                    description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus, labore commodi? Recusandae eligendi placeat a omnis. Non praesentium nihil mollitia cumque repellat, at',
                },
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/mixins' as *;
@use '../../styles/partials/variables' as *;

section#service-solution {
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
        margin-bottom: 2.5rem;
    };
    .container {
        @include flex (row, space-between, center)
    }
}
</style>