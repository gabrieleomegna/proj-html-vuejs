<template>
    <section id="award">
        <div id="container-different">
            <span>Headache free</span>
            <h2>Award Winning Moving Company</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum eos ad et voluptate ab, alias natus dignissimos? Provident nobis cumque ad totam non id magnam, vero similique repudiandae neque debitis.</p>
            <ButtonComponent :size="'small'"
                             :content="'Read Our Testimonials'"/>
        </div>
    </section>
</template>
<script>
import ButtonComponent from '../smallComponents/ButtonComponent.vue';
export default {
    components: {
        ButtonComponent
    }
}
</script>
<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;
@use '../../styles/partials/mixins' as *;

section#award {
    background-color: $section-award-bg;
    padding: 8rem 3rem;
    div#container-different{
        width: 40%;
        margin: 0 auto;
        @include flex (column,space-between, center);
        span{
            color: rgb(170, 170, 170);
            font-size: .75rem;
            font-weight: 900;
            text-transform: uppercase;
            margin-bottom: .5rem;
        }
        p,
        h2 {
            text-align: center;
            margin-bottom: 1.5rem
        };
        p {
            font-size: .8rem;
            font-weight: 500;
            opacity: $main-text-opacity;
            line-height: 1.5rem;
        };
        h2 {
            width: 70%;
            font-size: 2.2rem;
            font-weight: 900;
        }
    }
}
</style>