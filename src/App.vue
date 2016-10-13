<template>

	<div v-if="user.isAdmin">
		Es Esmu Admins
		<strong>{{user.name}}</strong>
		<button @click="logOut()">LogOut</button>
	</div>

	<div v-if="!user.isAdmin">
		Es Esmu Parasts Lietotajs
 	<input v-model="user.name">
	<input type="password" v-model="user.pass">
	<button @click="authorize(user.name, user.pass)">LogIn</button>
	</div>

	<pre>{{ user | json }}</pre>

</template>

<script>
export default {
 	data () {
 		return {
   			user: {
    			name: "",
     			pass: "",
     			isAdmin: false
   			}
		}
 	},
 	methods: {
 		authorize (username, password) { 
 			console.log(username)
 			if (username == "ww" && password == "ww") {
 				this.user.isAdmin = true
 			} else {
 				this.user.pass = ""
 			}

 		},
 		logOut () {
 			this.user.isAdmin = false
 		}

 	}
}
</script>

<style>

</style>