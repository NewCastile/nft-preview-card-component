<!-- @format -->

<script setup lang="ts">
import { ref } from "vue"

defineProps<{ image: string }>()
const hovered = ref<boolean>(false)
</script>

<template>
	<div
		class="card-image-container"
		v-on:mouseenter="() => (hovered = true)"
		v-on:mouseleave="() => (hovered = false)"
	>
		<div
			class="card-image-pane"
			:style="{ visibility: hovered ? `visible` : `hidden` }"
		>
			<img src="/public/images/icon-view.svg" alt="" />
		</div>
		<img class="card-image" :src="image" alt="" />
	</div>
</template>

<style>
.card-image-container {
	border-radius: 10px;
	position: relative;
	height: 300px;
}
.card-image {
	width: 100%;
	height: 100%;
	border-radius: 10px;
}
.card-image-pane {
	position: absolute;
	width: 100%;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: hsla(178, 100%, 50%, 0.549);
	border-radius: 10px;
	cursor: pointer;
}
</style>
