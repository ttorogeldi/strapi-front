<template>
  <v-container>

  </v-container>
</template>

<script>
import axios from 'axios'
  export default {
    name: 'HelloWorld',
    mounted() {
    axios.get('localhost:1337/api/restaurant',{
      headers:{
        Authorization:
            'Bearer '+ localStorage.getItem('token'),
      }
    })
      },
    data: () => ({
    }),
  }
</script>
