<template>
    <div class="container">
        <section class="find-product">

            <!-- Text  -->
            <div class="text">
                    
                <!-- Title  -->
                <p class="title primary-color">
                    Find a freshly baked product perfect for you
                </p>

                <!-- Description  -->
                <div class="desc tertiary-color">
                    Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis at leo feugiat placerat. Sed ac nulla id orci tempor convallis sed.
                </div>

                <!-- Button  -->
                <a class="btn secondary-color" href="#">Start Shopping</a>

            </div>

            <!-- Product slider  -->
            <div class="products-slider">

                <!-- Slider Buttons  -->
                <SliderButtons @setIndexes="updateIndexes"/>

                <!-- Product Card  -->
                <ProductCard :productObject="product" :type="'small'" v-for="(product, index) in productsToShow" :key="index"/>

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
    },
    props: {
        productsArray: Array
    },
    data: function() {
        return {
            activeIndexes: [0, 1, 2, 3]
        }
    },
    methods: {
        updateIndexes: function(toDo) {
            toDo === 'increase' ? this.activeIndexes = this.increaseIndexes() : this.activeIndexes = this.decreaseIndexes();
        },
        increaseIndexes: function() {
            const newIndexes = [];
            const activeIndexes = this.activeIndexes;
            this.activeIndexes = [];  

            activeIndexes.forEach((activeIndex) => {
                if (activeIndex < this.productsArray.length - 1) {
                    newIndexes.push(activeIndex + 1); 
                }else {
                    newIndexes.push(0);
                }        
            });
            return newIndexes
        },
        decreaseIndexes: function() {
            const newIndexes = [];
            const activeIndexes = this.activeIndexes;
            this.activeIndexes = [];

            activeIndexes.forEach((activeIndex) => {
                if (activeIndex > 0) {
                    newIndexes.push(activeIndex - 1); 
                }else {
                    newIndexes.push(this.productsArray.length - 1); 
                }                
            });
            return newIndexes;
        }
    },
    computed: {
        productsToShow() {
            const products = [];

            this.productsArray.forEach((product, index) => {
                if(this.activeIndexes.includes(index)) {
                    products.push(product);
                }
            });

            return products;
        }
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