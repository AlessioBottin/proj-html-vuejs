<template>
    <div class="slider-buttons">
        <!-- Previous  -->
        <div @click="$emit('setIndexes', 'decrease')" class="slider-btn">
            <i class="fas fa-chevron-left"></i>
        </div>

        <!-- Next  -->
        <div @click="$emit('setIndexes', 'increase')" class="slider-btn">
            <i class="fas fa-chevron-right"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SliderButtons',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.slider-buttons {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;

    .slider-btn {
        width: 40px;
        height: 80px;
        background-color: #a691b2dc;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;
        color: #d3c8d6;

        &:hover {
            z-index: 3;
            background-color: $brand_primary_color;
            color: $brand_secondary_color;
        }
    }
}
</style>