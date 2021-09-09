<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <test msg="Welcome to Your Vue.js App"/>

  <div>
    <ToggleText></ToggleText>
  </div>
  

  <div>
    Klicka här för att ändra texten:
    <EditableText 
    v-bind:text="editable"
    v-on:update="updatedText"></EditableText>
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

img {
  max-width: 200px;
}
</style>
