<template>
    <input v-model="textContent" placeholder="Type something ..."> 
    <p>{{ textContent }}</p>   
    <!-- <p>b{{ typeState }}</p>    -->
</template>

<script>
export default {
  name: 'InputByText',
  data() {
    return {
        textContent: ''
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