<template>
  <div class="hello">
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
import InputByText from './InputByText'
import InputByRadio from './InputByRadio'
import InputBySelect from './InputBySelect'
// import InputByText from './InputByText.vue'
// import InputByRadio from './InputByRadio.vue'
// import InputBySelect from './InputBySelect.vue'

export default {
  name: 'HelloWorld',
  data() {
    return {
      }
  },
  components: {
    InputByText,
    InputByRadio,
    InputBySelect,
  },
  props: {
    typeState: String
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
