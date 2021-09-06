<template>
  <div class="hello">
    <h1> Vue demo projekt </h1>
    <p>{{ exempel }}</p>
    <button v-show="showButton" v-on:click="handleClick"> Hejsan </button>
    <button v-show="!showButton"> Jag är osynlig </button>
    
    <h3>Lucas</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">GitHub</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">LinkedIn</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    exempel: 'Detta är ett exempel på data property.',
    showButton: true
  }),
  methods: {
    handleClick() {
      console.log('Inside handleClick');
      this.showButton = !this.showButton
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
