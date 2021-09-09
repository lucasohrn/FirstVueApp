<template>
<div>
    <span v-show="showText" v-on:click="handleClick"> {{ text }} </span>
    <input v-show="!showText" type="text" v-model="text2" v-on:blur="handleBlur">
    {{text2}}
</div>
</template>

<script>
export default {
    props: ['text'],
    data: () => ({
        showText: true,
        text2: ''
    }),
    methods: {
        handleClick() {
            this.showText = false
        },
        handleBlur() {
            this.$emit('update', this.text2)
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
