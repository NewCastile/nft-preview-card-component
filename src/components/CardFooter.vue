<!-- @format -->

<script setup lang="ts">
defineProps<{
	creator: {
		picture: string
		name: string
	}
}>()
</script>

<template>
	<hr />
	<div class="card-footer">
		<img class="card-footer-img" :src="creator.picture" alt="" />
		<p>
			Creation of <a href="">{{ creator.name }}</a>
		</p>
	</div>
</template>

<style>
.card-footer {
	display: flex;
	flex-direction: row;
	justify-content: flex-start;
	align-items: center;
}
.card-footer-img {
	height: 35px;
	border: 1px solid white;
	border-radius: 100%;
}
.card-footer > * + * {
	padding-left: 10px;
}
hr {
	color: hsl(215, 32%, 27%);
}
</style>
