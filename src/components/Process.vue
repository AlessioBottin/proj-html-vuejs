<template>
    <div class="container">
        <section class="process">

                <!-- Step 1  -->
                <div class="banner big">
                    <div class="overlay">

                        <!-- Left Column  -->
                        <div class="col-l">
                            <div class="title secondary-color">
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
                            <div class="title secondary-color">
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
                        <div class="title primary-color">
                            “Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity.”
                        </div>

                        <!-- By  -->
                        <div class="desc tertiary-color">
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
                            <div class="title secondary-color">
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
    </div>
</template>

<script>
export default {
    name: 'Process',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.process {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            color: $brand_secondary_color;

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
</style>