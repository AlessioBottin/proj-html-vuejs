<template>
    <div class="card">
        <img :src="require('../assets/img/choco-chip-cookies-500x638.jpg')" alt="cookies">
    </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props: {
        type: String,
        productsArray: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.card {
    width: 522px;
}

</style>