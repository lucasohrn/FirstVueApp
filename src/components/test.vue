<template>
<div>


  <div>
      <p>{{counter}}</p>
      <button @click="counterSub">-1</button>
      <button @click="counterAdd">+1</button>
  </div>

  <div>
      <div v-show="counter > 2">
          <h1>Some Text</h1>
          <p>Hello {{counter}}</p>
          <div v-for="(item, index) in items"
          :key="index">
          <p>my item {{item}}</p>
          <p>this index is: {{index}}</p>
          </div>
      </div>
  </div>

  <div v-bind:class="{ active: isActive }">God morgon</div>
  <button @click="changeActive">XXX</button>

  <div>{{ panan }}</div>

  </div>
</template>


<script>
export default {
    data() {
        return {
            counter: 0,
            isActive: true,
            items: ["kalle", "jocke", "maggan"]
        }
    },

    computed: {
        panan() {
            return "banan";
        }  
    },

    methods: {
        changeActive() {
            this.active = !this.active;
        },
        counterAdd() {
            this.counter += 1;
        },
        counterSub() {
            this.counter -=1;
        }
    }
}
</script>

<style>

.active {
    color: tomato;
}

</style>