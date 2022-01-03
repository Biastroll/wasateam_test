<template>
    <h2>Choose the type of input.</h2>
    <div>
      <input v-model="typeState" type="radio" id="choice_a" name="input-select" value="text">
      <label for="choice_a">text</label>
      <input v-model="typeState" type="radio" id="choice_b" name="input-select" value="radio">
      <label for="choice_b">radio</label>
      <input v-model="typeState" type="radio" id="choice_c" name="input-select" value="select">
      <label for="choice_c">select</label>
      <div v-if="typeState">
        <span>input type : {{ typeState }}</span>  
      </div>
    </div>
  <HelloWorld :typeState="typeState"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'App',
  data() {
    return {
      typeState: '',
      }
  },
  components: {
    HelloWorld,
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
</style>
