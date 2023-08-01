<script >
import inputComponents from './components/inputComponents.vue'
import wellcomeComponent from './components/welcomeComponent.vue'
import welcomeByHourComponent from './components/welcomeByHourComponent.vue'
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
  },
  components: {
    inputComponents,
    wellcomeComponent,
    welcomeByHourComponent
  }
}
</script>

<template>
  <div>
    <wellcomeComponent :msg="text"></wellcomeComponent>
    <welcomeByHourComponent :name="text"></welcomeByHourComponent>
    <div>
      <a href="https://vitejs.dev" target="_blank">
        <img src="/vite.svg" class="logo" alt="Vite logo" />
      </a>
      <a href="https://vuejs.org/" target="_blank">
        <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
      </a>
    </div>
    <inputComponents :msg="text" @onInputHandler="onInputHandler"></inputComponents>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
