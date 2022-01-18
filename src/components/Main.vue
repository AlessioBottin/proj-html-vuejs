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

            <!-- Product creation process  -->
            <section class="process">

                <!-- Step 1  -->
                <div class="banner big">
                    <div class="overlay">

                        <!-- Left Column  -->
                        <div class="col-l">
                            <div class="title secondary">
                                Tell us what you have in mind
                            </div>
                        </div>

                        <!-- Right Column  -->
                        <div class="col-r">

                            <!-- Step Number  -->
                            <p class="small-title step">01</p>

                            <!-- Description  -->
                            <div class="description">
                                <div class="small-title">manual ingredient selection</div>
                                <div class="desc">
                                    Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat, finibus in velit placerat, rutrum augue.
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Step 2  -->
                <div class="banner small">
                    <div class="overlay">

                        <!-- Left Column  -->
                        <div class="col-l">

                            <!-- Title  -->
                            <div class="title secondary">
                                We start baking
                            </div>

                            <!-- Description  -->
                            <div class="description">
                                <div class="small-title">sweet & delicious</div>
                                <div class="desc">
                                    Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat, finibus in velit placerat.
                                </div>
                            </div>
                        </div>

                        <!-- Right Column  -->
                        <div class="col-r">
                            <p class="small-title step">02</p>
                        </div>

                    </div>
                </div>

                <!-- Quote  -->
                <div class="banner small">
                    <div class="quote">
                        
                        <!-- Title  -->
                        <div class="small-title">
                            dont just take words for it
                        </div>

                        <!-- Text  -->
                        <div class="title primary">
                            “Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity.”
                        </div>

                        <!-- By  -->
                        <div class="desc tertiary">
                            Rachel Cooper, Founder
                        </div>

                    </div>
                </div>

                <!-- Step 3 -->
                <div class="banner big">
                    <div class="overlay">

                         <!-- Left Column  -->
                        <div class="col-l">

                            <!-- Title  -->
                            <div class="title secondary">
                                Delivered to your home
                            </div>

                            <!-- Description  -->
                            <div class="description">
                                <div class="small-title">baked to order & gift wrapped</div>
                                <div class="desc">
                                    Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat, finibus in velit placerat, rutrum augue.
                                </div>
                            </div>
                        </div>

                        <!-- Right Column  -->
                        <div class="col-r">
                            <p class="small-title step">03</p>
                        </div>

                    </div>
                </div>
            </section>

            <!-- Locations  -->
            <section class="locations">

                <!-- Title  -->
                <div class="text">
                    <div class="small-title">
                        locations
                    </div>

                    <div class="title primary">
                        Visit our Bakeries
                    </div>
                </div>

                <!-- Info Container  -->
                <div class="info-container">

                    <!-- Left Banner  -->
                    <div class="banner box">
                        <img :src="require('../assets/img/new-york-bk.jpg')" alt="new york bk">
                    </div>

                    <!-- Right Banner  -->
                    <div class="banner box">                        
                        <img :src="require('../assets/img/london-bk.jpg')" alt="london bk">
                    </div>

                    <!-- Left Info Box -->
                    <div class="box info">

                        <!-- Location  -->
                        <div class="title primary">New York</div>

                        <!-- Info  -->
                        <div class="info-text">

                            <!-- Phone Number  -->
                            <div class="phone-number small-title">
                                <p>call us</p>
                                <p>1.800.458.556</p>
                            </div>

                            <!-- Working hours -->
                            <div class="working-hours small-title">
                                <p>open all week</p>
                                <p>9:00 AM – 6:00 PM</p>
                            </div>

                            <!-- Map  -->
                            <a class="btn primary" href="#">View Map</a>

                        </div>

                    </div>

                    <!-- Right Info Box  -->
                    <div class="box info">

                        <!-- Location -->
                        <div class="title primary">London</div>

                        <!-- Info -->
                        <div class="info-text">

                            <!-- Phone Number  -->
                            <div class="phone-number small-title">
                                <p>call us</p>
                                <p>1.800.458.556</p>
                            </div>

                            <!-- Working hours -->
                            <div class="working-hours small-title">
                                <p>open all week</p>
                                <p>9:00 AM – 6:00 PM</p>
                            </div>

                            <!-- Map  -->
                            <a class="btn primary" href="#">View Map</a>
                        </div>

                    </div>

                </div>

            </section>

            <!-- Socials  -->
            <section class="socials">

                <div class="box">
                    <img :src="require('../assets/img/social-1.jpg')" alt="social photo">
                </div>

                <!-- Follow us -->
                <div class="box box-wide"></div>

                <div class="box">
                    <img :src="require('../assets/img/social-2.jpg')" alt="social photo">
                </div>

                <div class="box">
                    <img :src="require('../assets/img/social-3.jpg')" alt="social photo">
                </div>

                <div class="box">
                    <img :src="require('../assets/img/social-4.jpg')" alt="social photo">
                </div>
                <div class="box">

                    <img :src="require('../assets/img/social-5.jpg')" alt="social photo">
                </div>
                <div class="box">

                    <img :src="require('../assets/img/social-6.jpg')" alt="social photo">
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
        
        // Product creation process 
        .process {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            color: white;

            // Banners
            .banner {
                margin-bottom: 50px;

                // Overlay Effect 
                .overlay {
                    display: flex;
                    justify-content: space-between;
                    width: 100%;
                    height: 100%;
                    background-color: rgba(0, 0, 0, 0.342);
                        
                }
                
                // Big Banners
                &.big {
                    width: 100%;
                    height: 810px;
                    
                    .overlay {
                        padding: 85px;                        

                        .col-l {
                            width: 40%;
                            display: flex;
                            flex-direction: column;
                            justify-content: space-between;                            
                        }

                        .col-r {
                            width: 35%;
                            display: flex;
                            flex-direction: column;
                            justify-content: space-between;                                                      
                        }

                        // Common 
                        .title {
                            font-size: 56px;
                        }

                        .step {
                            text-align: right;
                            font-size: 96px;
                            color: $brand_secondary_color;
                            font-weight: 200;
                        }

                        div.small-title {
                            margin-bottom: 20px;
                            color: #c0b9b9;
                        }
                    }
                    
                }

                // Small Banners
                &.small {   
                    width: 48%;
                    height: 780px;
                    background-color: #f6f0f2;
                    
                    // Left Banner 
                    .overlay{
                        padding: 50px;

                        // Left Column 
                        .col-l {
                            width: 55%;
                            display: flex;
                            flex-direction: column;
                            justify-content: space-between;

                            .title {
                                font-size: 56px;
                            }

                            div.small-title {
                                margin-bottom: 20px;
                                color: #c0b9b9;
                            }
                        }

                        // Right Column 
                        .col-r {
                            width: 35%;     

                            .step {
                                text-align: right;
                                font-size: 96px;
                                color: $brand_secondary_color;
                                font-weight: 200;
                            }    
                        }
                    }

                    // Right Banner 
                    .quote {
                        padding: 85px 100px;
                        height: 100%;
                        display: flex;
                        justify-content: center;
                        flex-direction: column;

                        .title {
                            margin: 30px 0;
                            font-size: 48px;
                        }
                    }
                }

                // Backgrounds 
                &:first-child {
                    background-image: url(../assets/img/bakery-process-1.jpg); 
                }

                &:nth-child(2) {
                    background-image: url(../assets/img/bakery-process-2.jpg);
                    background-size: cover;
                    background-position-x: right;
                }

                &:last-child {
                    background-image: url(../assets/img/bakery-process-3.jpg);
                    background-size: 2215px;
                    background-position-x: center;
                }

            }         
        }

        // Locations 
        .locations {

            // Title 
            .text {
                text-align: center;
                margin-bottom: 60px;

                .small-title {
                    margin-bottom: 25px;
                }
            }

            // Info Container 
            .info-container {
                display: flex;
                flex-wrap: wrap;

                .box {
                    width: 50%;
                }

                .info {
                    padding: 50px 70px;
                    text-align: center;
                    
                    &:nth-child(3) {
                        background-color: #f1f9fb;
                    }

                    &:last-child {
                        background-color: #faf3e3;
                    }

                    // Info 
                    .info-text {
                        display: flex;
                        justify-content: space-between;
                        align-items: flex-start;
                        margin-top: 40px;

                        div p:last-child {
                            font-size: 16px;
                            margin-top: 10px;
                        }
                    }
                }
            }
        }

        // Socials 
        .socials {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

            .box {
                width: 23%;
                margin-bottom: 50px;
                

                &-wide {
                    width: 49%;
                    background-color: #f3eef4;
                }
            }
        }
    }
}
</style>