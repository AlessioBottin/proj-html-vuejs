<template>
    <div class="container">
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
    </div>
</template>

<script>
export default {
    name: 'Locations',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

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
</style>