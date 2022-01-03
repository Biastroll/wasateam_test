<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      <input v-model="typeState" type="radio" id="choice_a" name="input-select" value="text">
      <label for="choice_a">text</label>
      <input v-model="typeState" type="radio" id="choice_b" name="input-select" value="radio">
      <label for="choice_b">radio</label>
      <input v-model="typeState" type="radio" id="choice_c" name="input-select" value="select">
      <label for="choice_c">select</label>
      <p>input type : {{ typeState }}</p>  
    </div>
    <div v-if="typeState=='text'">
      <input-by-text typeState />
    </div>
    <div v-else-if="typeState=='radio'">
      <input-by-radio />
    </div>
    <div v-else-if="typeState=='select'">
      <input-by-select />
    </div>
  </div>
</template>

<script>
import InputByText from './InputByText.vue'
import InputByRadio from './InputByRadio.vue'
import InputBySelect from './InputBySelect.vue'

export default {
  name: 'HelloWorld',
  data() {
    return {
      typeState: '',
      }
  },
  components: {
    InputByText,
    InputByRadio,
    InputBySelect,
  },
  props: {
    msg: String,
  },
  methods: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
