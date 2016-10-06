<template>
 <span class="platenumberdecor"> Plate Number </span>  <span class="platenumber">{{ car.plateNumber }}</span>
<div class="horsePower"> Horse Power <span class="color600"> {{ car.horsePower }} </span>  </div>

<span v-if="isCoolCar(car)"> ahuennna </span>
<span v-if="price(car)"> leta mashina </span>
</template>

<script>
export default {
	data () { 
		return {
			car:{
				plateNumber: "AA-3333",
				horsePower: 1200,
				price: 111,
			}
		}
	},
	methods: {
		isCoolCar (car) {
			return (car.horsePower > 1000)
		},	
		price (car) {
			return (car.price < 3000)
		}
	}

} 

</script>

<style>

.platenumberdecor{
	color: orange;

}

	.platenumber{
		color: red;
}

	.horsePower{
		color: green;

	}

	.color600{
		color: red;

	}

 
</style>

