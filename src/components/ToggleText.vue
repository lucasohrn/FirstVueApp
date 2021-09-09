<template>
<div>
    <button v-on:click="hideText"> {{buttonText}} </button>
    <br>
    <span v-show="textIsVisible">Now you see me</span> 
    <span v-show="!textIsVisible">Now you dont</span> 
</div>
    
</template>

<script>
export default {
    data: () => ({
        textIsVisible: true
    }),
    computed: {
        buttonText() {
            if(this.textIsVisible) {
                return 'Göm texten'
            }
            else {
                return 'Visa texten'
            }
        }
    },
    methods: {
        hideText() {
            this.textIsVisible = !this.textIsVisible
        }
    }
}
</script>

<style scoped>
div {
  border: 1px solid grey;
  padding: 1em;
}
</style>