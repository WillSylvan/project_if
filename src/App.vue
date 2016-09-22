<template>
<input type="text" v-model="username"> <br>
<input type="text"> <br>
<input type="submit" @click="submit()">

<div v-if="!username.length">
You Must Provide Data! Bitch
</div> 

</template>

<script>
export default {
  data () {
    return {
      username: ""
    }
  },
  methods: {
      submit() {
          if(this.username == "suka") {
          alert("yoo")

          }

      }
  }

}

</script>

<style>
</style>
