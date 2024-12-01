<template>
	<div class="article-wrapper">
		<div class="article">
			<span class="red-line"></span>
			<h2 class="section-title">Политика</h2>
			<h1 class="article-title">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.
			</h1>
			<p class="byline">
				Александр Новиков | Опубликовано: 21 фев, 2024, 21:08 | Изменено: 21 фев, 2024, 22:31
			</p>
			<img src="../../assets/first.png" alt="Фотография статьи" class="article-image" />
			<h3 class="subtitle">
				Volutpat ac tincidunt vitae semper. Felis bibendum ut tristique et egestas quis ipsum
				suspendisse.
			</h3>
			<p class="text">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Volutpat ac tincidunt vitae semper. Felis bibendum ut
				tristique et egestas quis ipsum suspendisse. Consequat id porta nibh venenatis. Cursus
				euismod quis viverra nibh cras pulvinar mattis nunc.
			</p>
			<h2 class="article-title">
				Rhoncus aenean vel elit scelerisque mauris pellentesque pulvinar pellentesque habitant.
			</h2>
			<p class="text">
				Volutpat ac tincidunt vitae semper. Felis bibendum ut tristique et egestas quis ipsum
				suspendisse. Consequat id porta nibh venenatis. Cursus euismod quis viverra nibh cras
				pulvinar mattis nunc. Id aliquet lectus proin nibh. Donec massa sapien faucibus et molestie.
			</p>
			<p class="text">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua. Volutpat ac tincidunt vitae semper. Felis bibendum ut
				tristique et egestas quis ipsum suspendisse. Consequat id porta nibh venenatis. Cursus
				euismod quis viverra nibh cras pulvinar mattis nunc.
			</p>
			<img src="../../assets/second.png" alt="Фотография статьи" class="article-image" />
			<p class="text">
				Rhoncus aenean vel elit scelerisque mauris pellentesque pulvinar pellentesque habitant.
				Imperdiet dui accumsan sit amet nulla facilisi morbi.
			</p>
			<p class="text">
				Volutpat ac tincidunt vitae semper. Felis bibendum ut tristique et egestas quis ipsum
				suspendisse.
			</p>
			<p class="text">
				Imperdiet dui accumsan sit amet nulla facilisi morbi. Tempor commodo ullamcorper a lacus
				vestibulum sed. Proin fermentum leo vel orci. In mollis nunc sed id semper risus in
				hendrerit.
			</p>
			<p class="text">Sed ullamcorper morbi tincidunt ornare massa eget egestas purus viverra.</p>
		</div>
		<!-- Правая колонка -->
		<aside class="sidebar">
			<div class="author-info">
				<img src="../../assets/author.png" alt="Фото автора" class="author-photo" />
				<h3 class="author-title">Об авторе</h3>
				<p class="author-name">Александр Новиков</p>
				<p class="author-text">
					Imperdiet dui accumsan sit amet nulla facilisi morbi. Tempor commodo ullamcorper a lacus
					vestibulum sed. Proin fermentum leo vel orci. In mollis nunc sed id semper risus in
					hendrerit. Sed ullamcorper morbi...
				</p>
			</div>
			<div class="related-materials">
				<span class="red-line"></span>
				<h3 class="related-title">Материалы по теме</h3>
				<ul class="related-list">
					<li class="related-item">
						<p>
							Imperdiet dui accumsan sit amet nulla facilisi morbi. Tempor commodo ullamcorper a
							lacus vestibulum sed.
						</p>
						<span class="related-topic">Тема</span>
					</li>
					<li class="related-item">
						<p>
							Imperdiet dui accumsan sit amet nulla facilisi morbi. Tempor commodo ullamcorper a
							lacus vestibulum sed.
						</p>
						<span class="related-topic">Тема</span>
					</li>
					<li class="related-item">
						<p>
							Imperdiet dui accumsan sit amet nulla facilisi morbi. Tempor commodo ullamcorper a
							lacus vestibulum sed.
						</p>
						<span class="related-topic">Тема</span>
					</li>
				</ul>
			</div>
		</aside>
	</div>
</template>

<script>
export default {
	name: 'ArticlePolitic'
}
</script>

<style>
.article-wrapper {
	display: flex;
	max-width: 1200px;
	margin: 80px auto;
	padding: 10px;
}

.article {
	width: 65%;
	padding-right: 20px;
	border-right: 1px solid #ddd;
}

.sidebar {
	width: 35%;
	padding-left: 20px;
}

.author-info {
	background-color: #f9f9f9;
	padding: 20px;
	border: 1px solid #ddd;
	border-radius: 8px;
	margin-bottom: 20px;
	text-align: left;
}

.author-photo {
	width: 80px;
	height: 80px;
	border-radius: 50%;
	object-fit: cover;
	margin-bottom: 10px;
}

.author-title {
	font-size: 20px;
	margin-bottom: 8px;
	color: #333;
}

.author-name {
	font-weight: bold;
	font-size: 18px;
	margin-bottom: 8px;
}

.author-text {
	font-size: 14px;
	color: #555;
	line-height: 1.4;
}

.related-materials {
	background-color: #f9f9f9;
	padding: 15px;
	border: 1px solid #ddd;
	border-radius: 8px;
}

.related-title {
	font-size: 18px;
	margin-bottom: 10px;
	color: #333;
}

.related-list {
	list-style: none;
	padding: 0;
	margin: 0;
}

.related-item {
	font-size: 14px;
	color: #555;
	margin-bottom: 8px;
}
.related-materials {
	font-family: Arial, sans-serif;
	margin: 0px;
}

.red-line {
	display: block;
	width: 50px;
	height: 4px;
	background-color: red;
	margin-bottom: 10px;
}

.related-title {
	font-size: 18px;
	font-weight: bold;
	margin-bottom: 10px;
}

.related-list {
	list-style-type: none;
	padding: 0;
}

.related-item {
	border-bottom: 1px solid #ddd;
	padding: 10px 0;
}

.related-item p {
	margin: 0 0 5px;
	font-size: 16px;
	color: #333;
}

.related-topic {
	font-size: 14px;
	color: gray;
	font-style: italic;
}

.red-line {
	display: block;
	width: 50px;
	height: 3px;
	background-color: red;
	margin-bottom: 10px;
}

.section-title {
	font-family: 'Roboto Condensed';
	font-weight: normal;
	font-size: 24px;
	color: #333;
	margin-bottom: 16px;
}

.article-title {
	font-size: 36px;
	color: #000;
	margin-bottom: 20px;
}

.byline {
	font-size: 14px;
	color: #555;
	margin-bottom: 20px;
}

.article-image {
	width: 100%;
	height: auto;
	margin-bottom: 20px;
}

.text {
	font-size: 16px;
	line-height: 1.6;
	margin-bottom: 16px;
}

@media screen and (max-width: 768px) {
	.article-wrapper {
		flex-direction: column;
	}

	.article {
		width: 100%;
		padding-right: 0;
		border-right: none;
		margin-bottom: 20px;
	}

	.sidebar {
		width: 100%;
		padding-left: 0;
	}
}
</style>
