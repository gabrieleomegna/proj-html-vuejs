<template>
    <article class="service-card">
        <div class="img-card">
            <img src="../../assets/img/avada-movers-serviceonephoto-final.jpg" alt="">
        </div>
        <div class="description-card">
            <h3>Two Man Teams</h3>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus, labore commodi? Recusandae eligendi placeat a omnis. Non praesentium nihil mollitia cumque repellat, at</p>
            <div class="card-btn-container">
                <ButtonComponent :size="'small'"
                                 :content="'Read More'"/>
            </div>
        </div>
    </article>
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
article.service-card{
    width: calc((100%/3) - 2rem);
    padding: 1rem;
    background-color: $card-bg;
    .img-card {
        margin-bottom: .5rem;
        img {
        width: 100%;
        }
    }
    .description-card {
        padding: .5rem;
        *:not(button) {
            text-align: center;
            margin-bottom: 1rem;
        }
        h3 {
            color: $card-title-color;
            font-size: 1.2rem;
            font-weight: 800;
        }
        p {
            font-size: .7rem;
            font-weight: 500;
            line-height: 1.3rem;
            opacity: $main-text-opacity;
            margin-bottom: 1.5rem;
        }
        .card-btn-container{
            text-align: center;
        }
    }
}
article.service-card > * {
        background-color: white;
    }
</style>