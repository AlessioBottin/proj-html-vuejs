<template>
    <main>
        <div class="container">

            <!-- Our Products  -->
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

            <!-- Corporate and weddings -->
            <section class="weddings">

                <!-- Title  -->
                <div class="text">
                    <div class="small-title">
                        corporate & weddings
                    </div>

                    <div class="title primary">
                        Baking Special Moments
                    </div>
                </div>

                <!-- Photos  -->
                <div class="photos">

                    <!-- Photo n1  -->
                    <div class="photo">

                        <!-- Default Image  -->
                        <div class="default">
                            <img :src="require('../assets/img/corporate-bg.jpg')" alt="wedding organization pic">
                        </div>

                        <!-- Hover Image  -->
                        <div class="hover">
                            <img :src="require('../assets/img/corporate-hover-bg.jpg')" alt="wedding organization pic">

                            <!-- Cta  -->
                            <div class="cta">

                                <!-- Title  -->
                                <div class="small-title">
                                    International Bakery
                                </div>

                                <!-- Description  -->
                                <div class="title secondary">
                                    Corporate Events
                                </div>

                                <!-- Button  -->
                                <a class="btn secondary" href="#">Explore More</a> 
                            </div>                            
                        </div>

                    </div>

                    <!-- Photo n2  -->
                    <div class="photo">

                        <!-- Default Image  -->
                        <div class="default">
                            <img :src="require('../assets/img/wedding-bg.jpg')" alt="wedding organization pic">
                        </div>

                        <!-- Hover Image  -->
                        <div class="hover">
                            <img :src="require('../assets/img/wedding-hover-bg.jpg')" alt="wedding organization pic">

                            <!-- Cta  -->
                            <div class="cta">

                                <!-- Title  -->
                                <div class="small-title">
                                    private dining hall
                                </div>

                                <!-- Description  -->
                                <div class="title secondary">
                                    Weddings & Parties
                                </div>

                                <!-- Button  -->
                                <a class="btn secondary" href="#">Explore More</a>                           
                            </div>
                            
                        </div>
                    </div>

                </div>


            </section>

            <!-- Find a product  -->
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
    </main>
</template>

<script>
import SliderButtons from './SliderButtons.vue';
import ProductCard from './ProductCard.vue';

export default {
    name: 'Main',
    components: {
        SliderButtons,
        ProductCard
    },
    data: function() {
        return {
            products: [
                
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

main {
    
    .container {

        // Spacing beetween sections 
        section {
            margin-top: $section_margin_top;
        }
        
        // Products 
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

        // Corporate Weddings 
        .weddings {

            // Title 
            .text {
                text-align: center;
                margin-bottom: 60px;

                .small-title {
                    margin-bottom: 25px;
                }
            }

            // Photos 
            .photos {
                display: flex;
                justify-content: space-between;

                .photo {
                    width: 46%; 

                    // Hover effect 
                    &:hover .hover {
                        display: block;
                    }
                    &:hover .default {
                        display: none;
                    }
                    
                    // .default {

                    // }

                    .hover {
                        display: none;
                        position: relative;

                        .cta {
                            position: absolute;
                            left: 50%;
                            top: 50%;
                            transform: translate(-50%, -50%);
                            text-align: center;
                            
                            .small-title {
                                margin-bottom: 25px;
                                color: white;
                            }

                            .title {
                                margin-bottom: 25px;
                            }
                        }
                    }
                }
            }
        }

        // Find a Product 
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
        
        
    }
}
</style>