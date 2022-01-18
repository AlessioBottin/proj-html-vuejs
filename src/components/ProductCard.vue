<template>
    <div class="card" :class="cardSize">
        
        <!-- Product image  -->
        <img :src="require('../assets/img/choco-chip-cookies-500x638.jpg')" alt="cookies">

        <!-- Product info for small slider  -->
        <div class="product-info" v-if="type === 'small'">

            <!-- Name  -->
            <div class="product-name primary">
                Choco Chip Cookies
            </div>

            <!-- Price  -->
            <div class="product-price primary">
                $19.00 - $39.00
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props: {
        type: String,
        productsArray: Array
    },
    computed: {
        cardSize() {
            return this.type;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.card {

    &.small {
        width: 280px;
    }

    &.big {
        width: 522px;
    }

    // test 
    img {
        width: 100%;
    }

    .product-info {
        text-align: center;

        .product-name {
            font-family: $font_title_family;
            font-weight: bold;
            font-size: 22px;
            margin: 20px 0;
        }

        .product-price {
            font-family: $font_desc_family;
        }
    }
}

</style>