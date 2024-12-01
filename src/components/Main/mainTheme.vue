<script setup>
import { ref } from 'vue'

const titles = ref([
	{ id: 1, title: 'СПОРТ', img: new URL('@/assets/rapper.png', import.meta.url).href },
	{ id: 2, title: 'ТУРИЗМ', img: new URL('@/assets/brige.png', import.meta.url).href },
	{ id: 3, title: 'ПАРТНЕРЫ', img: new URL('@/assets/islam.png', import.meta.url).href },
	{ id: 4, title: 'ПРОЕКТЫ', img: new URL('@/assets/september11.png', import.meta.url).href }
])
</script>

<template>
	<div>
		<div class="themes__bg" />
		<div class="wrapper">
			<div class="horizontal-line"></div>
			<div class="red-rectangle"></div>
			<h3>ТЕМЫ</h3>
			<div class="container">
				<div v-for="item in titles" :key="item.id" class="item">
					<h2 class="theme__title">{{ item.title }}</h2>
					<img :src="item.img" alt="Фотография статьи" />
					<p class="item_2-subtitle">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="w-[345px] h-[0px] border border-[#aaaaaa] mb-2 mt-2"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="w-[345px] h-[0px] border border-[#aaaaaa] mb-2 mt-2"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
					<div class="w-[345px] h-[0px] border border-[#aaaaaa] mb-2 mt-2"></div>
					<p class="item_2-list">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
.container {
	margin: 0 auto;
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: 357px;
	padding-bottom: 200px;
}

.themes__bg {
	width: 100%;
	height: 310px;
	background-color: black;
	position: absolute;
	z-index: -1;
	margin-top: -40px;
}

.theme__title {
	margin-top: 0;
	font-weight: bold;
	font-size: 32px;
	color: white;
}

h3 {
	margin-top: 16px;
	margin-bottom: 32px;
	font-size: 40px;
	font-weight: bold;
	color: white;
}

.horizontal-line {
	height: 0.3px;
	opacity: 1;
	width: 100%;
	background-color: white;
	margin: 0 auto;
}

.red-rectangle {
	width: 88px;
	height: 8px;
	background-color: #aa0000;
	margin-bottom: 10px;
}

.item_2-subtitle {
	font-family: 'Roboto Condensed';
	margin: 16px 0;
	font-size: 20px;
	font-weight: bold;
	width: 345px;
}

.item_2-list {
	width: 345px;
}

@media screen and (width < 769px) {
	.wrapper {
		margin-bottom: 20px;
		padding: 10px;
	}

	.theme__title {
		font-size: 20px;
	}

	img {
		width: 300px;
		height: 200px;
	}

	h3 {
		font-size: 20px;
	}

	.item:nth-child(n + 2) {
		display: none;
	}

	p {
		font-size: 16px;
	}
}
</style>
