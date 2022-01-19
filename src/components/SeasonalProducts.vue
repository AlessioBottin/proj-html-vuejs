<template>
    <section class="seasonal-products">
            <div class="container-s">
                <div class="flex-container">

                    <!-- Title  -->
                    <div class="small-title">
                        try our seasonal products
                    </div>

                    <!-- Cta  -->
                    <p class="cta title secondary">
                        Order for pick-up or delivery to your home
                    </p>

                    <!-- Button  -->
                    <a class="btn primary" chref="#">Shop Now</a>

                </div>
            </div>
    </section>
</template>

<script>
export default {
    name: 'SeasonalProducts',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.seasonal-products {
        width: 100%;
        background-image: url(../assets/img/call-to-action-bg.jpg);
        background-size: cover;
        padding: 100px 0;

        .container-s {

            .flex-container {
                
                .cta {
                    margin: 40px 0 70px 0;
                    font-size: 48px;
                    width: 60%;
                }
            }
        }
}
</style>