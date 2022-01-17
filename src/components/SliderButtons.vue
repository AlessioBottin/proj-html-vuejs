<template>
    <div class="slider-buttons">
        <!-- Previous  -->
        <div class="slider-btn">
            <i class="fas fa-chevron-left"></i>
        </div>

        <!-- Next  -->
        <div class="slider-btn">
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
        width: 50px;
        height: 100px;
        background-color: #a691b2;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;
        color: #d3c8d6;

        &:hover {
            z-index: 3;
            background-color: $brand_primary_color;
            color: white;
        }
    }
}
</style>