<template>
    <div>
        <button v-on:click="counter--">-</button>
        <span> {{totalCount()}} </span>
        <button v-on:click="counter++">+</button>
    </div>

</template>
    

<script>
export default {
    data() {
        return {
            counter: 0,
        }
    },
    methods: {
        totalCount: function() {
            if (this.counter <= 0) {
                this.counter = 0
            } else if (this.counter >= 10) {
                this.counter = 10
            }
            return this.counter
        },
    }
}
</script>

<style>
    button{
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        text-align: center; 
        background-color: #E9AFE3;
        color: #020202; 
        font-size: 18px;
        padding: 3px 5px;
        border: none;
    }
</style>