<template>
	<div>
		<section class="section">
			<div class="row">
				<div class="col-md-12 mt-5 px-5">
					<h1 class="page-title">Blog</h1>
				</div>
			</div>
		</section>
		<category-component/>
		<div class="row">
			<div class="col-md-9">
				<blog-post-component v-for="blog in blogs" :data="blog"/>	
			</div>
			<div class="col-md-3">
				<popular-article-component :populars="populars" :tags="tags"/>	
			</div>
		</div>
	</div>
</template>
<style>
	.page-title {
	    font-weight: bold;
	    color: #154276;
	}
</style>
<script>
	import CategoryComponent from '@/components/Home/Category/CategoryComponent.vue';
	import BlogPostComponent from '@/components/Home/BlogPost/BlogPostComponent.vue';
	import PopularArticleComponent from '@/components/Home/PopularArticle/PopularArticleComponent.vue';
	export default {
		name : 'home-comp',
		components : {
			CategoryComponent,
			BlogPostComponent,
			PopularArticleComponent,
			
		},
		data : function(){
			return {
				blogs : [
					{
						url : "hehe",
						img : 'ini gambar',
						title : 'ini judul',
						words : 'ini kata-kata',
						author : 'Andika K',
						post_date : '6 Maret 2019',
						view : 5,
					},
					{
						url : "hoho",
						img : 'ini gambar',
						title : 'ini judul 2',
						words : 'ini kata-kata 3',
						author : 'Andika K',
						post_date : '6 Maret 2019',
						view : 6,
					},
					{
						url : "hehe",
						img : 'ini gambar',
						title : 'ini judul',
						words : 'ini kata-kata',
						author : 'Andika K',
						post_date : '6 Maret 2019',
						view : 5,
					},
					{
						url : "hoho",
						img : 'ini gambar',
						title : 'ini judul 2',
						words : 'ini kata-kata 3',
						author : 'Andika K',
						post_date : '6 Maret 2019',
						view : 6,
					}
				],
				populars : [
					{
						url : 'populer',
						title : 'Bagaimana sih populer?',
					}
				],
				tags : [
					{
						url : 'tags',
						title : 'Tagssss',
					},
					{
						url : 'tags/1',
						title : 'Tagssss1',
					}
				],
				isOpen : false,
			}
		},

	};
</script>