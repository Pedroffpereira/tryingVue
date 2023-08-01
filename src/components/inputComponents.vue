<script >
export default {
    data() {
        return {
            text: 'Pedro Pereira'
        }
    },
    methods: {
        onInputHandler(event) {
            this.text = event.target.value;
        }
    }
}
</script>
<template>
    <div>
        <h1>{{ text }}</h1>
        <input type="text" v-on:input="(event) => onInputHandler(event)">
    </div>
</template>