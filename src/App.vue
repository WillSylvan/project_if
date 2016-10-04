<template>
	<ul>
		<li v-for="item in menu"
		v-bind:class="{ active: item.active }">
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
	}
}
</script>


<style>

.active{
	color: red;
}

</style>
