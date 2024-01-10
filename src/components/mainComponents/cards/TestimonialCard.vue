<template lang="">
    <article class="testimonial-card">
        <div class="card-img">
            <img src="../../../assets/img/avada-movers-johndoe-final.jpg" alt="">
        </div>
        <h3>Jhon Doe</h3>
        <p><em>"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores repellat, mollitia obcaecati ad sit soluta dignissimos saepe ea qui dolorum ducimus. Tempora dignissimos dolorum eligendi?"</em></p>
    </article>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
@use '../../../styles/partials/variables' as *;
@use '../../../styles/partials/mixins' as *;
article.testimonial-card {
    width: calc((100% / 3) - 2rem);
    margin-right: 1rem;
    @include flex (column,space-between,center);
    * {
        margin-bottom: 1.5rem;
    }
    .card-img {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        overflow: hidden;
        img {
            width: 100%;
        }
    };
    h3,
    p {
        text-align: center;
    };
    h3 {
        color: $card-title-color;
    };
    p{
        opacity: $main-text-opacity;
        font-size: .7rem;
        font-weight: 500;
        line-height: 1.5rem;
    }
}
</style>