<template>
    <button :class="size">
        {{ content }}
    </button>
</template>
<script>
export default {
    props : {
        size : {
            type: String,
            required: true
        },
        content : {
            type: String,
            required: true
        }
    }
    
}
</script>
<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    button {
        border: none;
        border-radius: 25px;
        background-color: $btn-bg-color;
        color: $btn-text-color;
        text-transform: uppercase;
        font-weight: 700;
    }
    .small {
        padding: .5rem 1.5rem;
        font-size: .7rem;
    }
    .big {
        padding: .8rem 2rem;
        font-size: .8rem;
    }
</style>