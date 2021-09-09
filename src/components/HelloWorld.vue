<template>
  <div class="hello">
    <h1> Snow White </h1>
    
    <head>
  <link href="https://fonts.googleapis.com/css?family=Open+Sans:300i,400" rel="stylesheet">
</head>
<body>
<div class="container">
  <div class="card">
    <h3 class="title">Kloker</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://th.bing.com/th/id/R.bfb775af7e2ff9637f50b10bd2148e91?rik=s2zF96y9JlA9hw&riu=http%3a%2f%2fpluspng.com%2fimg-png%2f7-dwarfs-png--1245.png&ehk=lg%2fvKwmLAOSIJxpyTgRttZaJQvttofRXAVNIeGSr09o%3d&risl=&pid=ImgRaw&r=0" alt="">
  </div>

  <div class="card">
    <h3 class="title">Blyger</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://cdn.quotesgram.com/img/30/79/365311253-500px-Bashful2.png" alt="">
  </div>

  <div class="card">
    <h3 class="title">Glader</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://vignette2.wikia.nocookie.net/disney/images/0/0e/Happy1.png/revision/latest?cb=20140105032753" alt="">
  </div>

  <div class="card">
    <h3 class="title">Prosit</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://vignette.wikia.nocookie.net/thedescendants/images/f/f9/Sneezy_transparent.png/revision/latest?cb=20160126150551" alt="">
  </div>

  <div class="card">
    <h3 class="title">Butter</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://vignette.wikia.nocookie.net/parody/images/4/4f/Grumpy2.png/revision/latest?cb=20141029225848" alt="">
  </div>

  <div class="card">
    <h3 class="title">Toker</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://1.bp.blogspot.com/-Bf81PsFMI5s/WJ-vv_8SKmI/AAAAAAAABDA/4k3ClyA3DpoEj9rs9bzBfPHu5O2Sx5jDgCLcB/s1600/Dopey.png" alt="">
  </div>

  <div class="card">
    <h3 class="title">Trötter</h3>
    <div class="bar">
      <div class="emptybar"></div>
      <div class="filledbar"></div>
    </div>
    <img src="https://th.bing.com/th/id/R.173326f17c021191b719f6c02f206c99?rik=6QCTBpBE4BGWvQ&riu=http%3a%2f%2fpluspng.com%2fimg-png%2fsleepy-dwarf-png-sleepy-bbs-png-978.png&ehk=F3xysD7%2bXLYVM9zMIYu1ZcmIfp8FNidk%2fKiMjiUAx6Q%3d&risl=&pid=ImgRaw&r=0" alt="">
  </div>
</div>

<div class="mathContainer">
  <section>
    <p>{{ counter }}</p>
    <button class="subaddbtn" v-show="mathButton" v-on:click="subtractionClick"> - </button>
    <button class="subaddbtn" v-show="mathButton" v-on:click="additionClick"> + </button>
  </section>
  
  <section>
    <button class="reset" v-show="mathButton" v-on:click="defaultValueClick"> Reset </button>
  </section>
  
  <section>
    <button class="reset" v-show="showButton" v-on:click="showButtonClick"> Now You See Me! </button>
  </section>
    
  <section>
    <button v-show="lightsButton" v-on:click="lightsOnClick" v-bind:class="[isActive ? 'white' : 'black']"> {{ Text }} </button>
  </section>

<section class="footer">
  <h3>Lucas</h3>
  <ul>
    <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">GitHub</a></li>
    <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">LinkedIn</a></li>
  </ul>
</section>
    
</div>


</body>
  </div>
</template>

<script>
export default {
  components: {
  },
  name: 'HelloWorld',
  data: () => ({
    showButton: true,
    mathButton: true,
    lightsButton: true,
    isActive: true,
    Text: 'Lights are ON',
    counter: 10,
    hej: true,
    editable: "Exempel",
    counters: [
      { id: 1, num: 0 },
      { id: 2, num: 0 },
      { id: 3, num: 0 }
    ]
  }),
  computed: {
    counterView() {
      return this.counter
    }
  },
  methods: {
    additionClick() {
      console.log('Inside additionClick');
      //this.showButton = !this.showButton;
      this.counter += 1;
    },
    subtractionClick() {
      console.log('Inside additionClick');
      //this.showButton = !this.showButton;
      this.counter -= 1;
    },
    defaultValueClick() {
      console.log('Inside defaultValueClick');
      //this.showButton = !this.showButton;
      this.counter = 10;
    },
    showButtonClick() {
      console.log('Inside defaultValueClick');
      this.showButton = !this.showButton;
    },
    hiddenButtonClick() {
      console.log('Inside defaultValueClick');
      this.showButton = !this.showButton;
    },
    lightsOnClick() {
      console.log('Inside lightsOn');
      //this.lightsButton = !this.lightsButton;
      this.isActive = !this.isActive;
      if (!this.isActive)
        this.Text = 'Lights are Off'
      else
        this.Text = 'Lights are On'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
head {
  background-color: rgba(70, 64, 64, 0.5);
}

button {
  font-size: 1em;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

section {
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

section button {
  font-size: 3em;
  margin-top: 0;
  margin-bottom: 1em;
}

.card img {
  height: 10em;
  margin-top: 110px;
  margin-left: 35px;
}

.footer {
  padding-bottom: 20px;
}

.mathContainer {
  margin-top: 330px;
  background:#2e3033;
}

.white
{
  background: whitesmoke;
}

.black
{
  background: rgba(70, 64, 64, 0.5);
  color: whitesmoke;
}

p {
  color: #5468a1;
  font-size: 5em;
  margin-bottom: 0.5em;
  margin-top: 0;
  padding-top: 0.5em;
}

.mathContainer .reset{
  position: relative;
  color:white;
  background-color: #5468a1;
  margin-left: 2px;
  margin-right: 2px;
  font-size: 2em;
}

.mathContainer .subaddbtn{
  position: relative;
  color:white;
  background-color: rgba(70, 64, 64, 0.5);
  width: 2em;
  height: 2em;
  margin-left: 5px;
  margin-right: 5px;
}

h1 {
  font-size: 2em;
}

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

body {
  margin: 0;
  background: lightgray;
  text-align: center;
  font-family: sans-serif;
  color: #fefefe;
}
.container {
  position: relative;
  width: 320px;
  margin-top: 100px;
  perspective: 1000px;
}

.carousel {
  position: absolute;
  width: 100%;
  height: 100%;
  transform-style: preserve-3d; 
  animation: rotate360 60s infinite forwards linear;
}
.carousel__face { 
  position: absolute;
  width: 300px;
  height: 187px;
  top: 20px;
  left: 10px;
  right: 10px;
  background-size: cover;
  box-shadow:inset 0 0 0 2000px rgba(0,0,0,0.5);
  display: flex;
}

span {
  margin: auto;
  font-size: 2rem;
}

body {
  background-color: #100e17;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

.container {
  position: absolute;
  height: 300px;
  width: 1000px;
  top: 60px;
  left: calc(50% - 500px);
  display: flex;
  margin-top: 300px;
}

.card {
  display: flex;
  height: 280px;
  width: 200px;
  background-color: #5468a1;
  border-radius: 10px;
  box-shadow: -1rem 0 3rem #000;
/*   margin-left: -50px; */
  transition: 0.4s ease-out;
  position: relative;
  left: 0px;
}

.card:not(:first-child) {
    margin-left: -50px;
}

.card:hover {
  transform: translateY(-20px);
  transition: 0.4s ease-out;
}

.card:hover ~ .card {
  position: relative;
  left: 50px;
  transition: 0.4s ease-out;
}

.title {
  color: white;
  font-weight: 300;
  position: absolute;
  left: 20px;
  top: 15px;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

.bar {
  position: absolute;
  top: 100px;
  left: 20px;
  height: 5px;
  width: 150px;
}

.emptybar {
  background-color: #2e3033;
  width: 100%;
  height: 100%;
}

.filledbar {
  position: absolute;
  top: 0px;
  z-index: 3;
  width: 0px;
  height: 100%;
  background: rgb(0,154,217);
  background: linear-gradient(90deg, rgba(0,154,217,1) 0%, rgba(217,147,0,1) 65%, rgba(255,186,0,1) 100%);
  transition: 0.6s ease-out;
}

.card:hover .filledbar {
  width: 120px;
  transition: 0.4s ease-out;
}

.circle {
  position: absolute;
  top: 150px;
  left: calc(50% - 60px);
}

.stroke {
  stroke: rgb(192, 28, 28);
  stroke-dasharray: 360;
  stroke-dashoffset: 360;
  transition: 0.6s ease-out;
}

svg {
  fill: #17141d;
  stroke-width: 2px;
}

.card:hover .stroke {
  stroke-dashoffset: 100;
  transition: 0.6s ease-out;
}

</style>
