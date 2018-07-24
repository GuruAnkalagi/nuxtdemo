<template>
	<section class="books">
		<book v-for="b in books" :key="b.id" :thumbnail="b.thumbnail" :title="b.title" :id="b.id" :desc="b.desc"></book>
		
	</section>
</template>

<style scoped>
	.books
	{
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: center;
	}
</style>

<script>
	import book from '@/components/book'
	export default {
		components: {
			book
		},
		asyncData() {
			return new Promise((resolve, reject) => {
				setTimeout(() => {
					resolve({
						books:[
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
						}]
					})
				}, 500)
			})
		}
	}
</script>