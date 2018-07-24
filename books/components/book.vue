<template>
<nuxt-link :to="'/books/'+ id">
	<article class="book">
			<div class="thumbnail" :style="{backgroundImage: 'url('+ thumbnail +')'}"></div>
			<h1>{{title}}</h1>
			<p>{{desc}}</p>
		</article>
</nuxt-link>
</template>
<style>
	a {
		text-decoration: none;
		color: black;
	}
	.thumbnail
	{
		background-position: center;
		background-size: cover;
		width: 100%;
		height: 200px;	
	}
	.book
	{
		box-sizing: border-box;
		width: 280px;
		padding: 8px;
		border:1px solid gray;
		box-shadow: 0 2px 3px #aaa;
		margin: 10px;
	}
</style>
<script>
	export default {
		props: ['thumbnail', 'title', 'desc',"id"]
	}
</script>
