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
    .small {
        background-color: blue;
    }
    .big {
        background-color: orange;
    }
</style>