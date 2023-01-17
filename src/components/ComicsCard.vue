<script>
export default {
    name: 'ComicsCard',
    props: {
        url: String,
        title: String
    }
}
</script>

<template>
    <div class="card-unit">
        <img :src="url" alt="" class="img-comics">
        <p class="text-under">{{ title }}</p>
    </div>
</template>

<style lang="scss">
    .card-unit{
        width: calc(100% / 7);
    }    

    .img-comics{
        object-fit: cover;
    }

    .text-under{
        font-size: 18px;
        text-transform: uppercase;
        padding-top: 10px;
        color: white;
    }
</style>