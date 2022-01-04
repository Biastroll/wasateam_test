<template>
    <!-- <button @click="imortApi">Get Api</button> -->
    <!-- <div>{{ jsonApi }}</div> -->
    <ul v-for="jsonApi in imortApi" :key="jsonApi.name">
      <li>{{ jsonApi.name }}</li>
      <li>{{ jsonApi.city }}</li>
    </ul>
</template>

<script>
import jsonApi from "../assets/fake data.json";


export default {
  name: 'Api',
  data(){
      return {
          apiItem: []
      }
  },
  props: {
  },
  mounted(){
  },
  methods: {
  },
  computed: {
    imortApi() {
      return jsonApi.map((item) => {
        return item;
      });
    },
  },
}
</script>