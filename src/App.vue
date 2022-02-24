<!-- @format -->

<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import styles from "./styles/global.css"
import Card from "./components/Card.vue"
import { INft } from "./types"
const nft: INft = {
	name: "Equlibrium",
	code: 3429,
	description: "Our Equilibrium collection promotes balance and calm.",
	price: 0.0041,
	time_left: 3,
	image: "/images/image-equilibrium.jpg",
}
</script>

<template>
	<Card :nft="nft"></Card>
	<footer :style="{ marginTop: '4rem' }" class="attribution">
		Challenge by
		<a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
			>Frontend Mentor</a
		>. Coded by
		<a href="https://github.com/NewCastile" target="_blank">New Castile</a>.
	</footer>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600&display=swap");
@import url("./styles/global.css");
#app {
	text-align: center;
	margin: 0 auto;
	height: 100%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}

a {
	color: hsl(0, 0%, 100%);
	text-decoration: none;
}

a:hover {
	color: hsl(178, 100%, 50%);
}
</style>
