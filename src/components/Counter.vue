<template>
	<div>
		<h1>{{ count }}</h1>
		<button v-on:click="decrease"> <p>-</p> </button>
		<button v-on:click="increase"> <p>+</p> </button>
		<button v-on:click="reset"> <p>Återställ</p> </button>
	</div>
</template>

<script>
export default {
	data: () => ({
		count: 10
	}),
	methods: {
		increase() {
			this.count += 1
		},
		decrease() {
			this.count -= 1
		},
		reset() {
			this.count = 10
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
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: 1.4em;
  margin: 0.1em;
  background-color: rgb(99, 99, 99);
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
h1 {
	color: #5468a1;
	font-size: 3.4em;
	margin-bottom: 0em;
	margin-top: 0;
	padding-top: 0em;
}
</style>