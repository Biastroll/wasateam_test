<template>
    <input v-model="textChoice" type="radio" id="choice_a" name="radios" value="option A">
    <label for="choice_a">option A</label>
    <input v-model="textChoice" type="radio" id="choice_b" name="radios" value="option B">
    <label for="choice_a">option B</label>
    <input v-model="textChoice" type="radio" id="choice_c" name="radios" value="option C">
    <label for="choice_a">option C</label>
    <p>{{ textChoice }}</p>   
</template>

<script>
export default {
  name: 'InputByRadio',
  data(){
      return {
          textChoice: ''
      }
  },
  props: {
  },
  methods: {
  }
}
</script>