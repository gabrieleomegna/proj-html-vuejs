<template>
    <section id="request-free-quote">
        <div id="container-different">
            <h2>
                Request A Free Quote
            </h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae corporis delectus est perspiciatis ad necessitatibus fugit mollitia debitis minima assumenda blanditiis ipsum aliquid, excepturi commodi autem ab quia praesentium. Vero.</p>
            <div id="btn-container">
                <ButtonComponent :size="'small'"
                                 :content="'Click Here'"/>
            </div>
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
    @use '../../styles/partials/mixins' as *;
    @use '../../styles/partials/variables' as *;
    section#request-free-quote {
        background-image: url('../../assets/img/avada-movers-request-quote-background.jpg');
        padding: 8rem 0;
        div#container-different {
            width: 60%;
            margin: 0 auto;
            padding: 0 3rem;
            *:not(button) {
                margin-bottom: 2rem;
                text-align: center
            };
            div#btn-contanier {
                @include flex (row, center, center);
            };
            p {
                font-size: .8rem;
                font-weight: 500;
                line-height: 1.5rem;
                opacity: $main-text-opacity;
            };
            h2 {
                margin-bottom: 1rem;
                font-size: 2.3rem;
                font-weight: 900;
            }
        }
    }
</style>