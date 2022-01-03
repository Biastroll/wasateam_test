<template>
  <HelloWorld msg="Choose the type of input."/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'App',
  // data() {
  //   return {
  //     inputTypeA: 'text',
  //     inputTypeB: 'radio',
  //     inputTypeC: 'select',
  //     }
  // },
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
