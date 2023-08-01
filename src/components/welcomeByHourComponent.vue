<script >
import { computed } from 'vue';

export default {
    name: 'Welcome',
    props: {
        name: String
    },
    methods: {
        getMesage() {
            const date = new Date();

            if (12 > date.getHours()) {
                return "Bom dia " + this.name
            }
            if (20 > date.getHours()) {
                return "Boa Tarde " + this.name
            }
            if (24 > date.getHours()) {
                return "Boa Noite " + this.name
            }

        }
    },

}
</script>
<template>
    <div>
        <h1>{{ getMesage() }}</h1>
    </div>
</template>