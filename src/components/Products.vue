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
                    <SliderButtons @setIndexes="updateIndexes"/>

                    <!-- Product Card  -->
                    <ProductCard :productObject="product" :type="'big'" v-for="(product, index) in productsToShow" :key="index"/>

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
    },
    props: {
        productsArray: Array
    },
    data: function() {
        return {
            activeIndexes: [0, 1],
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