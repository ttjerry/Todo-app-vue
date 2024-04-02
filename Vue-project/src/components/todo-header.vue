<template>
    <div class="container">
        <img src="../assets/bg-desktop-dark.jpg" alt="" class="header-image">
        <div class="centered-header">
            <h2>Todo</h2>
            <span><img src="../assets/icon-sun.svg" alt="mode"></span>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
* {
    margin: 0;
    padding: 0;
}

.container {
    position: relative;
    text-align: center;
}

.container img {
    width: 100%;
    padding: 0;
    margin: 0;
}

.centered-header {
    position: absolute;
    align-items: center;
    top: 45%;
    left: 50%;
    width: 43%;
    background-color: transparent;
    transform: translate(-50%, -50%);
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    h2 {
        font-size: 36px;
        text-transform: uppercase;
        letter-spacing: 12px;
        background-color: transparent;
        color: white;
    }

    span {
        color: white;
        background-color: transparent;
        img{
            background-color: transparent;
            width: 20px;
        }
    }
}
</style>