<template>
<div>
    <button v-on:click="hideText"> {{buttonText}} </button>
    <br>
    <span v-show="textIsVisible"> <p>Now you see me</p></span> 
    <span v-show="!textIsVisible"><p>Now you dont</p> </span> 
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
  border: 1px;
  padding: 1em;
  background-color: #2e3033;
}

button {
  font-size: 1em;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
</style>