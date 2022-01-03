<template>
    <div>{{ typeState }}</div>
    <!-- <div v-if="typeState='text'"> -->
        <input v-model="textContent" placeholder="Type something ..."> 
        <p>{{ textContent }}</p>   
    <!-- </div> -->
    <!-- <div v-else-if="typeState='radio'"> -->
        <input v-model="textChoice" type="radio" id="choice_a" name="radios" value="option A">
        <label for="choice_a">option A</label>
        <input v-model="textChoice" type="radio" id="choice_b" name="radios" value="option B">
        <label for="choice_b">option B</label>
        <input v-model="textChoice" type="radio" id="choice_c" name="radios" value="option C">
        <label for="choice_c">option C</label>
        <p>{{ textChoice }}</p>   
    <!-- </div> -->
    <!-- <div v-else> -->
        <select name="selection" v-model="textOption">
            <option value="">choose the option</option>
            <option value="A">A</option>
            <option value="B">B</option>
            <option value="C">C</option>
        </select>
        <p>{{ textOption }}</p>   
    <!-- </div> -->
</template>

<script>
export default {
  name: 'ChangeInput',
  data() {
    return {
        textContent: '',
        textChoice: '',
        textOption: ''
      }
  },
//   data(){
//       return {
//           textContent: ''
//       }
//   },
  props: {
    typeState: String
  },
  methods: {
    // changeType(){
    //   console.log(this.props)
    // }
  }
}
</script>