<script>
import axios from 'axios'

export default {
	name: 'mainGrid',
	data() {
		return {
			same_as_article: [],
			main_article: {},
			n: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.'
		}
	},
	mounted() {
		this.fetchMainArticle()
	},
	methods: {
		async fetchMainArticle() {
			try {
				const response = await axios.get('http://127.0.0.1:5000/data_main_page')
				this.main_article = response.data.main_article[0]
				this.same_as_article = response.data.same_as_main.slice(0, 3)
				console.log(this.same_as_article)
			} catch (error) {
				console.error('Error fetching main article:', error)
			}
		}
	}
}
</script>

<template>
	<div class="container">
		<div class="item item_1">
			<div class="item_1-one">
				<h3 class="item_1-title">
					{{ main_article.title }}
				</h3>
				<p class="item_1-subtitle">
					{{ main_article.subtitle }}
				</p>
				<div class="vertical-line"></div>
				<p class="item_1-text">Похожие новости</p>
				<ul class="item_1-list">
					<li v-for="article in same_as_article" :key="article.id">
						{{ article.title }}
					</li>
				</ul>
			</div>
			<div class="item_1-two">
				<img
					class="item_1-img"
					src="../../assets/comunicacion%20politica%20(1)%201.png"
					alt="123"
				/>
			</div>
		</div>
		<div class="item item_2">
			<div class="horizontal-line"></div>
			<div class="red-rectangle"></div>
			<h3 class="item_2-title">Последние новости</h3>
			<img
				src="../../assets/284320788be7027b8bea3f687155b7fb%201.png"
				alt="asd"
				style="width: 300px"
			/>
			<p class="item_2-subtitle">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.
			</p>
			<p class="asd font-bold">17 минут назад</p>

			<div v-for="n in 5">
				<div class="w-[345px] h-[0px] border border-[#aaaaaa] mb-2 mt-2"></div>
				<p class="item_2-list">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do.</p>
			</div>
		</div>
		<div class="item item_3">
			<img src="../../assets/1.png" alt="" class="mb-4" />
			<p class="dsa">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
			</p>
		</div>
		<div class="item item_4">
			<img src="../../assets/2.png" alt="" class="mb-4" />
			<p class="dsa">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
			</p>
		</div>
		<div class="item item_5">
			<img src="../../assets/3.png" alt="" class="mb-4" />
			<p class="dsa">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
			</p>
		</div>
	</div>
</template>

<style scoped lang="scss">
@import '@/styles/main.scss'; // Импортируем глобальные переменные и миксины

.container {
	margin: 0 auto;
	margin-top: 80px;
	width: 100%; // Изменяем ширину для адаптивности
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: repeat(2, 400px);
	gap: 32px 20px;

	// Адаптация под средние экраны
	@include media-max($screen-md) {
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: auto;
		gap: 20px;
	}

	// Адаптация под маленькие экраны
	@include media-max($screen-sm) {
		grid-template-columns: 1fr;
		grid-template-rows: auto;
		gap: 15px;
	}
}

.item_1 {
	display: flex;
	justify-content: space-between;
	grid-column: 1/4;

	@include media-max($screen-md) {
		grid-column: 1/3;
	}

	@include media-max($screen-sm) {
		flex-direction: column;
		align-items: center;
		grid-column: 1;
	}
}

.item_2 {
	max-width: 300px;
	grid-column: 4/4;
	grid-row: 1/3;

	@include media-max($screen-md) {
		grid-column: 2/2;
		grid-row: auto;
	}

	@include media-max($screen-sm) {
		grid-column: 1;
		max-width: 100%;
	}
}

.item_3,
.item_4,
.item_5 {
	@include media-max($screen-sm) {
		display: none;
	}
}

.horizontal-line,
.vertical-line {
	background-color: $black;
	opacity: 0.4;
}

.item_2-title {
	margin: 8px 0;
	font-weight: normal;

	@include media-max($screen-sm) {
		font-size: 16px;
	}
}

.item_2-subtitle {
	font-family: 'Roboto Condensed';
	margin: 8px 0;
	font-size: 20px;
	font-weight: bold;

	@include media-max($screen-sm) {
		font-size: 16px;
	}
}

.item_2-list {
	font-family: 'Roboto';
	font-size: 16px;

	@include media-max($screen-sm) {
		font-size: 14px;
	}
}

.asd {
	margin-top: 0;
	margin-bottom: 12px;
	color: $red;
	font-size: 12px;

	@include media-max($screen-sm) {
		font-size: 10px;
	}
}

.dsa {
	font-weight: 600;
	font-size: 18px;

	@include media-max($screen-sm) {
		font-size: 14px;
	}
}

.red-rectangle {
	width: 88px;
	height: 8px;
	background-color: $red;
}

.item_1-title,
.item_1-subtitle,
.item_1-text,
.item_1-list {
	padding: 10px;

	@include media-max($screen-sm) {
		font-size: 14px;
	}
}
</style>
