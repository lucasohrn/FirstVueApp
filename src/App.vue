<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <test msg="Welcome to Your Vue.js App"/>

  <div>
    <ToggleText></ToggleText>
  </div>
  

  <div class="test">
    <p>Klicka på äpplet för att skriva:</p> 
    <h1><EditableText 
    v-bind:text="editable"
    v-on:update="updatedText"></EditableText></h1>
    
  </div>
  
  <Counter></Counter>
  <Counter></Counter>
  <Counter></Counter>
</template>

<script>
import test from './components/HelloWorld.vue'
import Counter from './components/Counter.vue'
import EditableText from './components/EditableText.vue'
import ToggleText from './components/ToggleText.vue'

export default {
  name: 'App',
  components: {
    test,
    Counter,
    EditableText,
    ToggleText
  },
  data: () => ({
    editable: 'Exempel'
  }),
  methods: {
    updateText(data) {
      console.log('App: updatedText', data)
      this.editable = data
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.test {
  border: 1px;
  padding: 1em;
  background-color: #2e3033;
}
p {
	color: #ffffff;
	font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	font-size: 1.4em;
	margin-left: 0.2em;
	margin-right: 0.2em;
	margin-top: 0;
	margin-bottom: 0;
}
img {
  max-width: 200px;
}
</style>
