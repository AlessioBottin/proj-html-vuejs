<template>
    <div class="container">
        <section class="weddings">

            <!-- Title  -->
            <div class="text">
                <div class="small-title">
                    corporate & weddings
                </div>

                <div class="title primary-color">
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
                            <div class="title secondary-color">
                                Corporate Events
                            </div>

                            <!-- Button  -->
                            <a class="btn secondary-color" href="#">Explore More</a> 
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
                            <div class="title secondary-color">
                                Weddings & Parties
                            </div>

                            <!-- Button  -->
                            <a class="btn secondary-color" href="#">Explore More</a>                           
                        </div>
                        
                    </div>
                </div>

            </div>

        </section>
    </div>
</template>

<script>
export default {
    name: 'Weddings'
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';
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
                        color: $brand_secondary_color;
                    }

                    .title {
                        margin-bottom: 25px;
                    }
                }
            }
        }
    }
}
</style>