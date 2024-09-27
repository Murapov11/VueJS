<template>
  <div id="app">
    <AppHeader />
    <HelloWorld />
    <div class="counter">
      <h2>Counter: {{ counter.count }}</h2>
        <div v-if="counter.count == 0">
           <p>URA URA URA Counter EMPTY</p>
        </div>
      <button @click="counter.increment">Increment</button>
    </div>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'; // Make sure the name matches
import AppFooter from './components/AppFooter.vue'; // Make sure the name matches
import HelloWorld from './components/HelloWorld.vue';
import { useCounter } from './composables/useCounter.js';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    HelloWorld
  },
  setup() {
    const counter = useCounter();
    return { counter };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.counter {
  margin: 20px;
}
</style>