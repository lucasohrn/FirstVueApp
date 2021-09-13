<template>
    <div class="component">
        <h1> Simple AJAX </h1>
        <button v-on:click="sendRequest"> Send Request </button>
        <p> {{ message }} </p>
    </div>
</template>

<script>

export default {
    data: () => ({
        message: 'No response yet',
        countries : []
    }),
    methods: {
        async sendRequest() {
            const url = 'https://forverkliga.se/JavaScript/api/simple.php?world'
            try {
                // Fetch skickar ett GET request till URL
                console.log('first')
                const response = await fetch(url);
                console.log('second')
                const data = await response.json();
                console.log('Data from API:', data);
            }
            catch(error) {
                this.message = 'Something went wrong. Please try again later.'
                console.log(this.message);
            }
        }
    }
}
</script>

<style scoped>
.component {
    border: 1px solid gray;
    padding: 1em;
    margin: 1em;
}
p {
    color: indigo;
    margin-top: 2em;
}
</style>
