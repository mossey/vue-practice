<template>
  <div class="hello">
    <h1>{{ message }}</h1>


  </div>
</template>

<script>
  export default {
    name: 'hello',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App',
        message: 'welcome moses'
      }
    },
    created: function () {
      this.$http.get('http://salty-depths-59983.herokuapp.com').then(response => {
        console.log(response.data)
        // success callback
      }, response => {
        console.log('failed')
        // error callback
      })
    }
  }
</script>

