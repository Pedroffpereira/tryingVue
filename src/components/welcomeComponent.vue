<script >
export default {
    name: 'Welcome',
    props: {
        msg: String
    },

}
</script>
<template>
    <div>
        <h1>{{ msg }}</h1>
    </div>
</template>