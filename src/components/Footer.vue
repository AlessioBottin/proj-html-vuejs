<template>
    <footer>
        <div class="flex-container">

            <!-- Menu  -->
            <div class="menu">

                <!-- Logo  -->
                <div class="logo">
                    <img :src="require('../assets/img/avada-bakery-logo.png')" alt="avada bakery logo">
                </div>

                <!-- Nav-bar  -->
                <nav>
                    <ul class="link-list desc primary">

                        <li v-for="n in 7" :key="n">
                            <a class="active" href="#">home</a>
                        </li>
                        <li>
                            <a class="cart" href="#">
                                <i class="fas fa-shopping-cart"></i>
                                <span class="cart-items">0</span>
                            </a>
                        </li>
                    
                    </ul>
                </nav>

                <!-- Rights  -->
                <div class="rights desc">
                    © Copyright 2012-2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
                </div>


            </div>

            <!-- Newsletter  -->
            <div class="newsletter">

                <!-- Cta  -->
                <p class="cta title primary">Subscribe to our Newsletter</p>

                <!-- Email  -->
                <div class="email">
                    <input type="text" placeholder="Enter an email address*">
                    <a class="btn secondary" href="#">Subscribe</a>
                </div>

                <!-- Socials  -->
                <div class="social">
                    <ul class="social-list primary">
                        <li><i class="fab fa-instagram"></i></li>
                        <li><i class="fab fa-twitter"></i></li>
                        <li><i class="fab fa-facebook-f"></i></li>
                        <li><i class="fab fa-pinterest-p"></i></li>
                    </ul>
                </div>

            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

footer {
    padding: 70px;

    .flex-container {
        display: flex;
        justify-content: space-between;

        // Menu 
        .menu {
            width: 50%;
            
            // Logo 
            .logo {
                width: 160px;
                margin-bottom: 50px;
            }

            // Nav 
            nav {
                margin-bottom: 100px;

                .link-list {
                    display: flex;
                    justify-content: space-between;
                    text-transform: capitalize;

                    li {
                        .cart-items {
                            display: inline-block;
                            width: 20px;
                            height: 20px;
                            text-align: center;
                            line-height: 20px;
                            border-radius: 50%;
                            background-color: lightgray;
                            margin-left: 5px;
                        }
                    }
                }
            }

            // Rights 
            .rights {
                font-size: 13px;
                color: $brand_tertiary_color;
            }
        }

        // NewsLetter 
        .newsletter {
            text-align: right;

            // Cta 
            .cta {
                margin-bottom: 40px;
                font-size: 25px;
            }

            // Email 
            .email {
                margin-bottom: 147px;
                input {
                    padding: 15px;
                    width: 350px;
                    margin-right: 20px;
                    border: 1px solid $brand_tertiary_color;
                    outline: none;
                    border-radius: 5px;
                    font-family: $font_desc_family;
                }
            }
            
            // Social 
            .social  {
                .social-list {
                    display: flex;
                    justify-content: flex-end;

                    li {
                        margin: 0 15px;
                        font-size: 18px;
                    }
                }    
            }
        }
    }
}

</style>