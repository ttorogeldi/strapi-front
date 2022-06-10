<template>
  <v-container>
  </v-container>
</template>

<script>
import axios from 'axios'
  export default {
    name: 'HelloWorld',
    mounted() {
     /* axios
          .post('http://localhost:1337/api/auth/local', {
            identifier: 'string@gmail.com',
            password: 'string',
          })
          .then(response => {
            console.log(response)
            localStorage.setItem('token',response.data.jwt)
          })*/
      axios.get('http://localhost:1337/api/restaurants',{
        headers:{
          authorization:
              'Bearer '+ localStorage.getItem('token'),
        }
      }).then(res=>{
        console.log(res)
      }).catch(er=>{
        console.error(er)
      })
      },
    data: () => ({
    }),
  }
</script>
