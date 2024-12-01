<script setup></script>

<template>
	<div class="main__section">
		<div class="image-container">
			<img src="@/assets/main.png" alt="Main Image" class="main__image" />
		</div>
		<div class="main__container">
			<div class="main__title">ALLRUSSIA</div>
			<div class="main__subtitle">Мы открываем Россию заново! Вместе с вами!</div>
		</div>
	</div>
</template>

<style scoped lang="scss">
$screen-xs: 480px;
$screen-sm: 640px;
$screen-md: 768px;
$screen-lg: 1024px;
$screen-xl: 1280px;

.main__section {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	width: 100%;
	height: 100vh;
	position: relative;

	.image-container {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;

		.main__image {
			width: 100%;
			max-width: 100%;
			height: auto;
			object-fit: cover;
		}
	}

	.main__container {
		position: relative;
		text-align: center;
		color: white;
		z-index: 1;

		.main__title {
			font-size: 8vw;
			font-weight: bold;
			font-family: 'Roboto Condensed', sans-serif;
			margin-bottom: 20px;
		}

		.main__subtitle {
			font-size: 4vw;
			font-weight: bold;
			font-family: 'Roboto Condensed', sans-serif;
		}
	}
}

@media screen and (max-width: $screen-md) {
	.main__container {
		.main__title {
			font-size: 10vw;
		}

		.main__subtitle {
			font-size: 5vw;
		}
	}
}

@media screen and (max-width: $screen-sm) {
	.main__section {
		height: auto;
	}

	.main__container {
		.main__title {
			font-size: 12vw;
		}

		.main__subtitle {
			font-size: 6vw;
		}
	}
}

@media screen and (max-width: $screen-xs) {
	.main__section {
		padding: 10px;
	}

	.main__container {
		.main__title {
			font-size: 14vw;
		}

		.main__subtitle {
			font-size: 8vw;
		}
	}
}
</style>
