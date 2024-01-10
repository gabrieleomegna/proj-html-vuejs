<template>
    <section id="move-with-ease">
        <div class="container">
            <div id="block">
                <div id="diff-bg-color">
                    <span>We remove the headache from moving</span>
                    <h2>Move With Ease</h2>
                    <hr>
                    <p>With our super simple service we can take you from getting a quote, right through to being in your new home with all of your belongings securely packed and safely delivered, even in the rooms of your choice</p>
                    <ButtonComponent :size="'big'"
                                     :content="'Get a free quote now'"/>
                </div>
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
section#move-with-ease {
    padding: 7.5rem 0;
    background-image: url('../../assets/img/avada-movers-movewithease-background-new.jpg');
    background-size: cover;
    background-position: top
}
.container {
    @include flex (row-reverse, flex-start, center);
    #block {
        width: 50%;
        padding: .8rem;
        background-color: #5aa511;
        #diff-bg-color {
            padding: 2rem 1.7rem;
            background-color: #6abf17;
            @include flex (column, space-between, center);
            *:not(button) {
                color: white;
                margin-bottom: .8rem
            };
            hr {
                border: 1px solid #71db07;
                width: 295px;
            };
            h2{
                font-size: 2.2rem;
                font-weight: 800
            };
            span{
                text-transform: uppercase;
                font-weight: 800;
                font-size: .8rem;
                margin-bottom: .5rem;
            }
            p {
                margin-top: .5rem;
                text-align: center;
                font-size: .75rem;
                font-weight: 500;
                line-height: 1.7rem;
                margin-bottom: 1.8rem;
            }
        }
    }
}
    
</style>