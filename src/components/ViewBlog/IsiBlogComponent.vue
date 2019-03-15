<template>
	<div class="margin-top-400 ml-5">
		<div class="row mt-5">
			<div class="col-md-9">
				<div class="post-content-meta mb-5">{{ data.author }} — {{ data.post_date }}</div>
				<p>{{ data.words }}</p>
				<div class="tags f-14">
		    		<i class="fa fa-tag" aria-hidden="true"></i>
					<a v-for="tag in data.tags" :href="tag.url">{{ tag.name }}</a>
		        </div>
			</div>
			<div class="colmd-3 columns">
				<popular-article-component :populars="populars" :tags="tags"/>	
			</div>
		</div>	
	</div>
</template>
<style type="text/css">
	.margin-top-400{
		margin-top: 400px;
	}

	.post-content-share {
	    margin-top: 30px;
	    margin-bottom: 100px;
	}
</style>
<script type="text/javascript">
	import PopularArticleComponent from '@/components/Home/PopularArticle/PopularArticleComponent.vue';

	export default {
		name : 'isi-blog-component',
		components : {
			PopularArticleComponent,

		},
		data : function(){
			return {
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
				data : {
					author : 'Investree',
					post_date : '27 September 2018',
					words : 'Belajar Vue Nih',
					tags : [
						{
							url : '/hehe/tags',
							name : '#tags',
						},
						{
							url : '/hehe/tags/1',
							name : '#tags_1',
						},
						{
							url : '/hehe/tags/2',
							name : '#tags_3',
						}
					]
				}
			}
		}
	};
</script>