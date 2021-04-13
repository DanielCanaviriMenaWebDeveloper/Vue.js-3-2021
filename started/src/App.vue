<template>
	<div>
		<h1>Vue JS - 2021</h1>
		<!-- <p>Hola Daniel</p> -->
		<!-- <Car /> -->
		<CarComposition />
		<CarOptions />
	</div>
</template>

<script>
/* import Car from './components/Car'; */
import CarComposition from './components/CarComposition';
import CarOptions from './components/CarOptions.vue';
export default {
	components: {
		/* Car */
		CarComposition,
		CarOptions
	}
};
</script>

<style></style>
