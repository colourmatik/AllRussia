<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const sections = ref([
	{
		id: 1,
		title: 'ПОЛИТИКА',
		items: [
			{
				id: 1,
				title: 'Item 1',
				img: new URL('@/assets/12%20(1).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 2,
				title: 'Item 2',
				img: new URL('@/assets/12%20(2).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 3,
				title: 'Item 3',
				img: new URL('@/assets/12%20(3).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 4,
				title: 'Item 4',
				img: new URL('@/assets/12%20(4).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			}
		]
	},
	{
		id: 2,
		title: 'КУЛЬТУРА И ИСТОРИЯ',
		items: [
			{
				id: 1,
				title: 'Item 1',
				img: new URL('@/assets/12%20(1).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 2,
				title: 'Item 2',
				img: new URL('@/assets/12%20(2).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 3,
				title: 'Item 3',
				img: new URL('@/assets/12%20(3).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			},
			{
				id: 4,
				title: 'Item 4',
				img: new URL('@/assets/12%20(4).png', import.meta.url).href,
				description:
					'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.'
			}
		]
	}
])
</script>

<template>
	<div>
		<div v-for="section in sections" :key="section.id" class="wrapper">
			<div class="horizontal-line"></div>
			<div class="red-rectangle"></div>
			<h3>{{ section.title }}</h3>
			<div class="container">
				<div v-for="item in section.items" :key="item.id" class="item">
					<RouterLink to="/politic">
						<img :src="item.img" :alt="item.title" />
					</RouterLink>
					<p>{{ item.description }}</p>
				</div>
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
@import '@/styles/main.scss';
.wrapper {
	margin-bottom: 90px;
}

.container {
	margin: 0 auto;
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: 357px;
	gap: 20px;
}

.horizontal-line {
	height: 1px;
	width: 100%;
	background-color: #000;
	margin: 0 auto;
}

.red-rectangle {
	width: 88px;
	height: 8px;
	background-color: #aa0000;
	margin-bottom: 10px;
}

h3 {
	font-size: 24px;
	font-weight: normal;
}

.item {
	text-align: center;
}

.item > p {
	font-family: 'Roboto Condensed';
	font-size: 16px;
	font-weight: bold;
	margin-top: 16px;
}

@media screen and (max-width: $screen-md) {
	.container {
		grid-template-columns: repeat(2, 1fr);
		gap: 15px;
	}

	h3 {
		font-size: 20px;
	}

	.item > p {
		font-size: 14px;
	}
}

@media screen and (max-width: $screen-sm) {
	.container {
		grid-template-columns: 1fr;
		gap: 10px;
	}

	h3 {
		font-size: 18px;
	}

	.item > p {
		font-size: 12px;
	}

	.item {
		display: block;
	}

	.item > img {
		width: 100%;
		height: auto;
	}
}

@media screen and (max-width: $screen-xs) {
	.wrapper {
		margin-bottom: 30px;
		padding: 5px;
	}

	.container {
		grid-template-columns: 1fr;
	}

	h3 {
		font-size: 16px;
	}

	.item > p {
		font-size: 10px;
	}
}
</style>
