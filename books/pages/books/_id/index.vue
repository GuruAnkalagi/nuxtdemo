<template>
	<section class="single-book">
		<h1>{{book.title}}</h1>
		<div>
			<img class="book-image" :src="book.thumbnail">
		</div>
		<p>{{book.desc}}</p>
	</section>
</template>

<style>
	.single-book {
		display: flex;
		flex-flow: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		padding: 30px;
	}
	.book-image {
		width: 100%;
		
	}
</style>

<script>
	export default {
		asyncData(context) {
			return new Promise((resolve, reject) => {
				setTimeout(() => {
					resolve({
						book:[
						{
							id:"1",
							title:"title1",
							desc:"title 1 description",
							thumbnail:"https://www.hdwallpapers.in/walls/green_sea_view-wide.jpg"
						},
						{
							id:"2",
							title:"title2",
							desc:"title 2 description",
							thumbnail:"http://7-themes.com/data_images/collection/9/4500938-summer-beach-wallpapers.png"
						}].find(el => el.id === context.params.id)
					})
				}, 1500)
			})
		}
	}
</script>
