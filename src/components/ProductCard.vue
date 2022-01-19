<template>
    <div class="card" :class="cardSize">

        <!-- Product image  -->
        <div class="product-img">
            <img :src="require(`../assets/img/products/${productObject.path}`)" :alt="productObject.name">

            <!-- Product Hover -->
            <div class="product-hover">

                <!-- Big Slider  -->
                <div class="big-slider" v-if="type === 'big'">

                    <!-- Product Name  -->
                    <div class="title product-name">
                        {{productObject.name}}
                    </div>

                    <!-- Product genre  -->
                    <div class="desc product-genre">
                        {{productObject.type}}, {{productObject.genre}}
                    </div>

                    <!-- Product Price  -->
                    <div class="desc product-price">
                        {{productObject.price}}
                    </div>

                </div>

                <!-- Small Slider  -->
                <div class="small-slider" v-else>
                    <a class="desc" href="#">select options</a> / <a class="desc" href="#">quick view</a>
                </div>

            </div>
        </div>


        <!-- Product Info for small slider  -->
        <div class="product-info" v-if="type === 'small'">

            <!-- Name  -->
            <div class="product-name primary">
                {{productObject.name}}
            </div>

            <!-- Price  -->
            <div class="product-price primary">
                {{productObject.price}}
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props: {
        type: String,
        productObject: Object
    },
    computed: {
        cardSize() {
            return this.type;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.card {

    &.small {
        width: 280px;
    }

    &.big {
        width: 522px;
    }
 
    .product-img {
        width: 100%;
        position: relative;

        img {
            width: 100%;
        }

        // Hover effect
        &:hover .product-hover {
            display: block;
        }

        // Hover 
        .product-hover {
            display: none;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            color: $brand_secondary_color;
            background-color: rgba(211, 211, 211, 0.52);

            // Big Slider 
            .big-slider {
                width: 100%;
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
                flex-direction: column;

                .product-name {
                    font-size: 28px;
                }

                .product-price{
                    font-size: 22px;
                }
            }

            // Small SLider 
            .small-slider {
                display: flex;
                align-items: center;
                justify-content: space-evenly;
                text-transform: uppercase;
                font-size: 16px;
                width: 100%;
                height: 100%;

                a:hover {
                    font-size: 16px;
                    color: $brand_tertiary_color;
                }
            }
        }
    }

    .product-info {
        text-align: center;

        .product-name {
            font-family: $font_title_family;
            font-weight: bold;
            font-size: 22px;
            margin: 20px 0;
        }

        .product-price {
            font-family: $font_desc_family;
        }
    }
}

</style>