<template>
    <div class="container">
        <section class="socials">

            <div class="box">
                <img :src="require('../assets/img/social-1.jpg')" alt="social photo">
            </div>

            <!-- Follow us -->
            <div class="box box-wide">

                <!-- Title  -->
                <div class="small-title">
                    made for sharing
                </div>

                <!-- Cta  -->
                <p class="title primary-color">Let's stay in touch</p>

                <!-- Button  -->
                <a class="btn secondary-color" href="#">
                    <i class="fab fa-instagram"></i> Follow Us
                </a>
            </div>
                
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
</template>

<script>
export default {
    name: 'Socials',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

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
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            p {
                margin: 30px 0;
            }

            a:hover {
                background-color: $brand_secondary_color;
            }
        }
    }
}
</style>