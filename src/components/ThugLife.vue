<script setup lang="ts">
	import { ref } from "vue";
</script>

<template>
	<div class="thug-life">
		<div class="picture">
			<!-- <img src="/beard.png" class="beard" /> -->
			<img src="/glass.png" class="glass" />
			<img src="/goldChain.png" class="goldChain" />
			<!-- <img src="/pipe.png" class="pipe" /> -->
		</div>
	</div>
</template>

<style lang="scss" scoped>
	@keyframes glass {
		from {
			top: 0;
			left: 0;
			transform: rotate(0);
		}
		to {
			top: 449px;
			left: 636px;
			transform: rotate(355deg);
		}
	}
	@keyframes goldChain {
		from {
			top: 0;
			left: 0;
			transform: rotate(0);
		}
		to {
			top: 581px;
			left: 676px;
			transform: rotate(355deg);
		}
	}
	.thug-life {
		position: relative;
		top: 0;
		left: 0;
		z-index: 3;
	}
	.picture {
		width: 100vw;
		height: 100vh;
		.glass {
			position: absolute;
			max-height: 31px;
			top: 449px;
			left: 636px;
			transform: rotate(355deg);
			animation-name: glass;
			animation-duration: 4s;
			animation-timing-function: ease-out;
		}
		.goldChain {
			position: absolute;
			max-height: 184px;
			top: 581px;
			left: 676px;
			transform: rotate(355deg);
			animation-name: goldChain;
			animation-duration: 4s;
			animation-timing-function: ease-out;
		}
		.beard {
			position: absolute;
			max-height: 43px;
			top: 489px;
			left: 654px;
			transform: rotate(355deg);
		}
		.pipe {
			position: absolute;
			max-height: 76px;
			top: 505px;
			left: 639px;
			transform: rotate(24deg);
		}
	}
</style>
