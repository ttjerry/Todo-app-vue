<template>
    <div class="container">
        <!-- <input type="radio" name="" id="radio"> -->
        <label class="container2">
            <input type="checkbox" checked="checked">
            <span class="checkmark"></span>
        </label>
        <input type="text" id="todotask" placeholder="Create a new todo...">
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
    width: 40%;
    padding: 20px;
    background-color: hsl(235, 24%, 19%);
    display: flex;
    // justify-content: space-between;
    align-items: center;
    position: relative;
    left: 50%;
    transform: translate(-50%, -150%);
    border-radius: 5px;

    #radio {
        width: 40px;
        padding: 0;
        border: none;
    }

    #todotask {
        background-color: hsl(235, 24%, 19%);
        border: none;
        outline: none;
        color: white;
        width: 80%;
        font-size: 15px;
    }

    .container2 {
        display: block;
        position: relative;
        padding-left: 35px;
        cursor: pointer;
        font-size: 20px;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
    }

    /* Hide the browser's default radio button */
    .container2 input {
        position: absolute;
        left: 25%;
        top: 25%;
        transform: translate(-50%, -50%);
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    /* Create a custom radio button */
    .checkmark {
        position: absolute;
        top: -10px;
        vertical-align: middle;
        left: 0;
        height: 20px;
        width: 20px;
        background-color: #eee;
        border-radius: 50%;
    }

    /* On mouse-over, add a grey background color */
    .container2:hover input~.checkmark {
        background-color: #ccc;
    }

    /* When the radio button is checked, add a blue background */
    .container2 input:checked~.checkmark {
        // background-color: #2196F3;
        background-image: linear-gradient hsl(192, 100%, 67%) to hsl(280, 87%, 65%);
        background-size: contain;
        background-repeat: repeat;
    }

    /* Create the indicator (the dot/circle - hidden when not checked) */
    .checkmark:after {
        content: "";
        position: absolute;
        display: none;
    }

    /* Show the indicator (dot/circle) when checked */
    .container2 input:checked~.checkmark:after {
        display: block;
    }

    /* Style the indicator (dot/circle) */
    .container2 .checkmark:after {
        top: 4px;
        left: 7.2px;
        width: 3px;
        height: 8px;
        // border-radius: 50%;
        border: solid white;
        border-width: 0 3px 3px 0;
        -webkit-transform: rotate(45deg);
        -ms-transform: rotate(45deg);
        transform: rotate(45deg);
    }

}
</style>