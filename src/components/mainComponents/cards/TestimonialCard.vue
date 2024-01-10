<template lang="">
    <article class="testimonial-card">
        <div class="card-img">
            <img :src="getImagePath(`../../../assets/img/${singleTestimonial.pathImage}`)" alt="">
        </div>
        <h3>{{singleTestimonial.name}}</h3>
        <p><em>{{singleTestimonial.description}}</em></p>
    </article>
</template>
<script>
export default {
    props: {
        singleTestimonial: {
            type: Object,
            required: true
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
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