<template>
    <div class="flex-container">
        <button @click="decrement()"><strong>-</strong></button>
        <div class="counter"><strong>{{ number }}</strong></div>
        <button @click="increment()"><strong>+</strong></button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number : 0
        }
    },
    methods : {
        increment() {
            if(this.number >=0 ) {
                this.number++;
            }
        },
        decrement() {
            if(this.number >0) {
                this.number--;
            }
        }
    }
}
</script>

<style>
    body{
        font-size: 20px;
    }
    .counter{
        padding: 20px;
    }
    .flex-container {
        padding: 0;
        margin: 0;
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    button{
        height: 40px;
        width: 40px;
        border-radius: 50%;
        border: 1px solid orange;
        background-color: orange;
        color: white;
        font-size: 20px;
        box-shadow: 2px 2px 2px darkgrey;
    }
</style>
