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
        padding: .5rem 1.5rem;
        border: none;
        border-radius: 25px;
        background-color: $btn-bg-color;
        color: $btn-text-color;
        text-transform: uppercase;
        font-weight: bold;
        font-size: .7rem;
        // .small {
        //     background-color: blue;
        // }
        // .big {
        //     background-color: orange;
        // }
    }
</style>