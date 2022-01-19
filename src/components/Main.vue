<template>
    <main>

        <!-- Our Products  -->
        <section>
            <Products :productsArray="products"/>
        </section>

        <!-- Corporate and weddings -->
        <section>
            <Weddings />
        </section>

        <!-- Find a product  -->
        <section>
            <FindProduct :productsArray="products"/>
        </section>

        <!-- Product creation process  -->
        <section>
            <Process />
        </section>

        <!-- Locations  -->
        <section>
            <Locations />
        </section>

        <!-- Socials  -->
        <section>
            <Socials />
        </section>

        <!-- Seasonal Products  -->
        <section>
            <SeasonalProducts />
        </section>

    </main>
</template>

<script>
import Products from './Products.vue';
import Weddings from './Weddings.vue';
import FindProduct from './FindProduct.vue';
import Process from './Process.vue';
import Locations from './Locations.vue';
import Socials from './Socials.vue';
import SeasonalProducts from './SeasonalProducts.vue';

export default {
    name: 'Main',
    components: {
        Products,
        Weddings,
        FindProduct,
        Process,
        Locations,
        Socials,
        SeasonalProducts
    },
    data: function() {
        return {
            products: [
                {
                    name: 'Choco Chip Cookies',
                    path: 'choco-chip-cookies.jpg',
                    genre: 'Pastries',
                    type: 'Cookies',
                    price: '$19.00 - $39.00'
                },
                {
                    name: 'Strawberry Jam Cookies',
                    path: 'strawberry-jam-cookies.jpg',
                    genre: 'Pastries',
                    type: 'Cookies',
                    price: '$24.00 - $62.00'
                },
                {
                    name: 'Strawberry Donut',
                    path: 'strawberry-donut.jpg',
                    genre: 'Pastries',
                    type: 'Donuts',
                    price: '$24.00 - $62.00'
                },
                {
                    name: 'Perfect Macarons',
                    path: 'perfect-macarons.jpg',
                    genre: 'Pastries',
                    type: 'Macarons',
                    price: '$18.00 - $52.00'
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

main {
    // Spacing beetween sections 
    section {
        margin-top: $section_margin_top;
    }  
}
</style>