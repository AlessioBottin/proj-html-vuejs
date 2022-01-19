<template>
    <main>

        <!-- Our Products  -->
        <section>
            <Products />
        </section>

        <!-- Corporate and weddings -->
        <section>
            <Weddings />
        </section>

        <!-- Find a product  -->
        <section>
            <FindProduct />
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