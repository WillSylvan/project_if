<template>
	<ul>
		<li v-for="item in menu"
		v-bind:class="{ active: item.active }"
		@click="goToPage(item)">
			{{ item.title }} 
		</li>
	</ul>



</template>

<script>
export default {
	data () {
		return {
			menu: [
				{
					title: "Home",
					active: true
				},
				{
					title: "Team",
					active: false
				},
				{
					title: "About",
					active: false
				},
				{
					title: "Contact",
					active: false
				},
				{
					title: "real cool",
					active: false
				},
			]
		}
	},
	methods: {
		goToPage(menuItem) {
			for (let i in this.menu) {
				this.menu[i].active = false
			}
		menuItem.active = true	
		}
	}
}
</script>


<style>

.active{
	color: red;
}

li:hover{

	color: blue;
}

</style>

