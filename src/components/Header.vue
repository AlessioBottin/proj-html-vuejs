<template>
    <section>
        <!-- Nav  -->
        <nav>
            <div class="logo">
                <img :src="require('../assets/img/avada-bakery-logo.png')" alt="avada bakery logo">
            </div>

            <div class="nav-bar">
                <ul>
                    <li v-for="n in 8" :key="n">
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a class="cart" href="#"><i class="fas fa-shopping-cart"></i></a>
                    </li>
                    
                </ul>
            </div>
        </nav>

        <!-- Jumbo  -->
        <div class="jumbo">
            <div class="container">
                <div class="text-column">
                    <!-- Small title  -->
                    <div class="small-title">
                        fresh & tasty bakery everyday
                    </div>

                    <!-- Big Title  -->
                    <div class="title primary">
                        The Perfect Fresh Bread
                    </div>

                    <!-- Desc  -->
                    <p class="desc tertiary">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, quo sint? In tenetur vitae molestias, obcaecati dolorum ipsam, ratione aspernatur, velit veniam deleniti consequatur repudiandae laudantium porro laborum eaque sapiente!
                    </p>

                    <!-- Button  -->
                    <a class="btn primary" href="#">Explore our products</a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

section {
    background-image: url(../assets/img/hero-header-bakery.jpg);
    background-repeat: no-repeat;
    background-position-x: -270px;
    background-position-y: -95px;
    background-size: 2450px;;

    // Nav 
    nav {
        padding: 10px 25px 0 30px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        // Logo 

        // Nav Bar 
        .nav-bar {
            
            ul {
                display: flex;
                justify-content: space-between;

                li {
                    margin-left: 40px;
                    margin-top: 10px;
                    font-size: 12px;
                    color: $font_primary_color;

                    a {
                        font-family: $font_small_title_family;  
                        text-transform: uppercase;   
                    }

                    // Shopping cart 
                    // .cart {
                        
                    // }
                    
                }
            }
        }
    }

    // Jumbo 
    .jumbo {
        padding: 200px 0 295px 0;

        .container {

            .text-column {
                width: 30%;

                .small-title {
                    margin-bottom: 20px;
                }

                .title {
                    font-size: 60px;
                    margin-bottom: 30px;
                }

                .desc {
                    margin-bottom: 40px;
                }
            }
        }
    }
}

</style>