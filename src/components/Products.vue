<template>
    <div class="container">
        <section class="products">
                
                <!-- Text  -->
                <div class="text">
                    
                    <!-- Title  -->
                    <div class="small-title">
                        our products
                    </div>

                    <!-- Description  -->
                    <p class="title primary">
                        All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural, all organic ingredients.
                    </p>

                    <!-- Button  -->
                    <a class="btn secondary" href="#">Start Shopping</a>

                </div>

                <!-- Product slider  -->
                <div class="products-slider">

                    <!-- Slider Buttons  -->
                    <SliderButtons />

                    <!-- Product Card  -->
                    <ProductCard :productsArray="products" :type="'big'" v-for="n in 2" :key="n"/>

                </div>

            </section>
    </div>
</template>

<script>
import SliderButtons from './SliderButtons.vue';
import ProductCard from './ProductCard.vue';

export default {
    name: 'Products',
    components: {
        SliderButtons,
        ProductCard
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.products {
    display: flex;
    justify-content: space-between;

    // Text 
    .text {
        width: 32%;

        .small-title {
            margin-bottom: 20px;
        }

        .title {
            margin-bottom: 40px;
        }
    }

    // Products Slider 
    .products-slider {
        width: 63%;
        position: relative;
        display: flex;
        justify-content: space-between;   
    }
}
</style>