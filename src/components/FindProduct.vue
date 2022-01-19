<template>
    <div class="container">
        <section class="find-product">

                <!-- Text  -->
                <div class="text">
                    
                    <!-- Title  -->
                    <p class="title primary">
                        Find a freshly baked product perfect for you
                    </p>

                    <!-- Description  -->
                    <div class="desc tertiary">
                        Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis at leo feugiat placerat. Sed ac nulla id orci tempor convallis sed.
                    </div>

                    <!-- Button  -->
                    <a class="btn secondary" href="#">Start Shopping</a>

                </div>

                <!-- Product slider  -->
                <div class="products-slider">

                    <!-- Slider Buttons  -->
                    <SliderButtons />

                    <!-- Product Card  -->
                    <ProductCard :productsArray="products" :type="'small'" v-for="n in 4" :key="n + 'mini-slider'"/>

                </div>

        </section>
    </div>
</template>

<script>
import SliderButtons from './SliderButtons.vue';
import ProductCard from './ProductCard.vue';

export default {
    name: 'FindProduct',
    components: {
        SliderButtons,
        ProductCard
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.find-product {
            display: flex;
            justify-content: space-between;
            align-items: center;

            // Text 
            .text {
                width: 22%;
                text-align: center;

                .desc {
                    margin-bottom: 20px;
                }

                .title {
                    margin-bottom: 40px;
                }
            }

            // Products Slider 
            .products-slider {
                width: 70%;
                position: relative;
                display: flex;
                justify-content: space-between;   
            }
}
</style>