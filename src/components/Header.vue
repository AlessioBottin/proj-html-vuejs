<template>
    <header>
        <!-- Nav  -->
        <nav>
            <div class="logo">
                <img :src="require('../assets/img/avada-bakery-logo.png')" alt="avada bakery logo">
            </div>

            <div class="nav-bar">
                <ul>
                    <li v-for="(link, index) in menuLinksArray" :key="index">
                        <a :class="{ active : isActive(index)}" href="#">{{link.text}}</a>
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
                        Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Aliquam erat volutpat. Nullam quis sagittis nibh ac nulla id orci tempor.
                    </p>

                    <!-- Button  -->
                    <a class="btn primary" href="#">Explore our products</a>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        menuLinksArray: Array
    },
    data: function() {
        return {
            activeIndex: 0
        }
    },
    methods: {
        isActive(index) {
            return index === this.activeIndex ? true : false
        },
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

header {
    background-image: url(../assets/img/hero-header-bakery.jpg);
    background-repeat: no-repeat;
    background-position-x: -270px;
    background-position-y: -95px;
    background-size: 2450px;;

    // Nav 
    nav {
        padding: 10px 25px 0 25px;
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
                        line-height: 30px;
                        font-weight: bold;
                        
                        &.active {
                            border-bottom: 2px solid $brand_primary_color;
                        }
                    }

                    // Shopping cart 
                    
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
                    font-size: 56px;
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