<template>
    <NuxtLink :to="`/products/${card.id}`" class="card-container">
       <img class="image" :src="require(`@/assets/images/${card.image || 'fe1.png'}`)" alt="fe">
    </NuxtLink>
</template>
<script>
    export default {
        props:{
            card:{
                type: Object,
                default:() => {}
            }
        }
    }
</script>

<style  scoped>
    .card-container {
        width: 24%;
        height: 15rem;
        border-radius: 0.5rem;
        overflow: hidden;
        margin-bottom: 1.5rem;
        cursor: pointer;
    }

    .image {
        width: 100%;
        height: 100%
    }
</style>