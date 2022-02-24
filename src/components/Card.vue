<!-- @format -->

<script setup lang="ts">
import { INft } from "../types"
import CardFooter from "./CardFooter.vue"
import CardImage from "./CardImage.vue"

defineProps<{
	nft: INft
}>()
</script>

<template>
	<div class="card-container">
		<CardImage :image="nft.image"></CardImage>
		<section>
			<a class="nft-name" href="">{{ nft.name }} #{{ nft.code }}</a>
			<p class="nft-description">{{ nft.description }}</p>
			<div class="stack">
				<span class="nft-price">
					<img src="/images/icon-ethereum.svg" alt="" />
					<p>{{ nft.price }} ETH</p>
				</span>
				<span class="nft-time-left">
					<img src="/images/icon-clock.svg" alt="" />
					<p>{{ nft.time_left }} days left</p>
				</span>
			</div>
			<CardFooter
				:creator="{
					name: `Jules Wyvern`,
					picture: `/images/image-avatar.png`,
				}"
			></CardFooter>
		</section>
	</div>
</template>

<style>
section {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: flex-start;
}
.nft-name {
	font-size: 24px;
	font-weight: 600;
}
.nft-price {
	color: hsl(178, 100%, 50%);
}
.nft-price,
.nft-time-left {
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	font-weight: 600;
}
.nft-price > * + *,
.nft-time-left > * + * {
	padding-left: 10px;
}
.nft-description {
	text-align: left;
}
.stack {
	width: 100%;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
}
.stack p {
	line-height: 0%;
}
.card-container {
	margin: 0 auto;
	width: 300px;
	background-color: hsl(216, 50%, 16%);
	border-radius: 10px;
	padding: 30px;
	box-shadow: 0px 0px 25px 25px hsl(219, 51%, 11%);
}
.card-container > * + * {
	margin-top: 20px;
}
</style>
