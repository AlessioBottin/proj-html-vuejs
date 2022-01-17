<template>
    <section>
        <div class="buttons-container">
            <div class="button logo">
                <img :src="require('../assets/img/avada-logo.jpg')" alt="avada logo">
                <div>Demos</div>
            </div>
            <div class="button price">
                <div class="green dollar">$</div>
                <div class="green number">39</div>
                <div class="txt">On Sale</div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style lang="scss" scoped>
@import '../styles/utilities.scss';
@import '../styles/variables.scss';

.buttons-container {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 14px;
    position: fixed;
    top: 150px;
    right: 10px;

    .button {
        width: 65px;
        height: 65px;
        border-radius: 5px;
        background-color: white;
        color: black;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        box-shadow: 0px 0px 20px -5px #888888;
    }

    .logo {
        img {
            width: 30px;
            margin-bottom: 5px;
        }
        
    }
    .price {
        margin-top: 10px;
        position: relative;

        .dollar {
            position: absolute;
            top: 10px;
            left: 12px;
            font-size: 16px;
        }
        .number {
            position: absolute;
            top: 10px;
            right: 12px;
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 5px;
        }
        .green {
            color: #65bc7b;
        }
        .txt {
            position: absolute;
            top: 42px;
            left: 6px;
        }
    }
}
</style>