<template>
	<div class="main">
		<div class="banner">
			<h1 class="banner__headding">Южный федеральный округ</h1>
		</div>
		<div class="list">
			<div class="wrapper">
				<div class="list__top top">
					<span class="top__line-red line-red"></span>
					<p class="top__text text-headdind">ЦЕНТР ЮГА</p>
					<div class="top__card card">
						<img class="card__img" src="../../assets/rostov_flag.png" alt="" />
						<div class="card__box">
							<p class="card__headding">Ростов-на-Дону</p>
							<p class="card__text text-population">Население: 1 125 000 чел.</p>
							<p class="card__text text-square">Площадь: 354 км²</p>
							<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
						</div>
					</div>
				</div>
				<div class="list__bottom bottom">
					<span class="bottom__line-red line-red"></span>
					<p class="bottom__text text-headdind">Регионы</p>
					<div class="container__card">
						<div class="item item_1">
							<img src="../../assets/astrakhan_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Астраханская область</p>
								<p class="card__text text-population">Население: 999 000 чел.</p>
								<p class="card__text text-square">Площадь: 49 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_2">
							<img src="../../assets/volgograd_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Волгоградская область</p>
								<p class="card__text text-population">Население: 2 473 000 чел.</p>
								<p class="card__text text-square">Площадь: 112.9 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_3">
							<img src="../../assets/krasnodar_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Краснодарский край</p>
								<p class="card__text text-population">Население: 5 679 000 чел.</p>
								<p class="card__text text-square">Площадь: 75.5 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_4">
							<img src="../../assets/rostov_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Ростовская область</p>
								<p class="card__text text-population">Население: 4 202 000 чел.</p>
								<p class="card__text text-square">Площадь: 100.8 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_5">
							<img src="../../assets/adigea_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Республика Адыгея</p>
								<p class="card__text text-population">Население: 464 000 чел.</p>
								<p class="card__text text-square">Площадь: 7.8 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_6">
							<img src="../../assets/kalmykia_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Республика Калмыкия</p>
								<p class="card__text text-population">Население: 270 000 чел.</p>
								<p class="card__text text-square">Площадь: 74.7 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_7">
							<img src="../../assets/crimea_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">Республика Крым</p>
								<p class="card__text text-population">Население: 1 911 000 чел.</p>
								<p class="card__text text-square">Площадь: 26.9 тыс. км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
						<div class="item item_8">
							<img src="../../assets/sevastopol_flag.png" alt="" />
							<div class="item__card">
								<p class="card__headding">г. Севастополь</p>
								<p class="card__text text-population">Население: 512 000 чел.</p>
								<p class="card__text text-square">Площадь: 864 км²</p>
								<p class="card__text text-time">Часовой пояс: MSK (UTC+3)</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'SouthernFederalDistrict'
}
</script>

<style scoped>
.container__card {
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-template-rows: repeat(5, 225px);
	grid-column-gap: 90px;
	grid-row-gap: 60px;
}
.item {
	display: flex;
	justify-content: space-between;
}

.main {
	flex-direction: column;
	margin: 0;
}

p {
	margin: 0;
}

.wrapper {
	max-width: 1440px;
	margin: 0 auto;
}

/* banner */
.banner {
	background-image: url('@/assets/shapka.png');
	background-repeat: no-repeat;
	background-size: 100% 100%;
	min-height: 340px;
	display: flex;
	justify-content: center;
	align-items: center;
}

.banner__headding {
	font-size: 80px;
	font-weight: bold;
	color: #ffffff;
}

/* list */
.list {
	margin-top: 10px;
}

.list__top {
	border-top: 1px solid #aaaaaa;
}

.line-red {
	display: block;
	height: 13px;
	width: 80px;
	background-color: #aa0000;
}

.text-headdind {
	margin-bottom: 30px;
	margin-top: 24px;
	font-size: 24px;
	text-transform: uppercase;
}

.list__bottom {
	border-top: 1px solid #aaaaaa;
	margin-top: 80px;
}

.bottom__list-cards {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
}

/* card */
.card {
	display: flex;
	margin-top: 32px;
}

.card__box {
	display: flex;
	flex-direction: column;
	margin-left: 25px;
	justify-content: space-between;
}

.card__headding {
	margin-bottom: 57px;
	font-size: 36px;
}

.card__text {
	line-height: 2;
	font-size: 20px;
}

.bottom {
	margin-bottom: 80px;
}
/* //////////////////// */

/* media request */

@media screen and (width < 1400px) {
	.bottom__list-cards {
		justify-content: center;
	}

	.top__card {
		justify-content: center;
	}

	.banner__headding {
		font-size: 60px;
	}
}

@media screen and (width < 1000px) {
	.banner__headding {
		font-size: 45px;
	}
}

@media screen and (width < 769px) {
	.main {
		padding: 10px;
	}
	.container__card {
		grid-column-gap: 0;
		grid-row-gap: 30px;
		display: flex;
		flex-direction: column;
	}
	.item {
		flex-direction: column;
	}
	.card {
		flex-direction: column;
	}
	.card__headding {
		margin-bottom: 0;
	}
}
</style>
