<script setup>
	// This starter template is using Vue 3 <script setup> SFCs
	// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
	import ThugLife from "./components/ThugLife.vue";
	import { ref, watch } from "vue";
	const lottory = ["10", "16", "23", "26", "28", "29", "35", "41", "45"];
	const my = ref("");
	const res = ref();
	function check() {
		let myList = my.value.split(".");
		const initialValue = 0;
		res.value = lottory.reduce((accumulator, currentValue) => {
			console.log(myList.includes(currentValue), accumulator);
			if (myList.includes(currentValue)) {
				accumulator = accumulator + 1;
			}
			return accumulator;
		}, initialValue);
	}
	watch(my, (n, o) => {
		check();
	});
</script>

<template>
	<!-- <div class="me">
		<div class="picture">
			<img src="/1.臉部清晰的生活照.png" />
		</div>
		<ThugLife></ThugLife>
	</div> -->
	<input v-model="my" />
	{{ res }}
</template>

<style lang="scss" scoped>
	.me {
		position: relative;
		top: 0;
		left: 0;
		z-index: 1;
		.picture {
			position: relative;
			z-index: 2;
			width: 100vw;
			height: 100vh;
			display: flex;
			justify-content: center;
			align-items: center;
			img {
				max-height: 90vh;
			}
		}
	}
</style>
