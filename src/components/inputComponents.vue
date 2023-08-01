<script >
export default {

    props: {
        msg: String
    },
}
</script>
<template>
    <div>
        <h1>{{ msg }}</h1>
        <input type="text" v-on:input="(event) => this.$parent.onInputHandler(event)">
    </div>
</template>