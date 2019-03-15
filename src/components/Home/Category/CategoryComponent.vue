<template>
	<section class="section mt-5">
		<div class="row">
			<div class="col-md-12 col-sm-12">
				<ul class="blog-menu">
					<li v-for="cat in category">
						<a :href="cat.link">{{ cat.name }}</a>
					</li>
				</ul>
			</div>
		</div>
	</section>
</template>
<style>
	.blog-menu {
		list-style: none;
		margin-left: 0;
		margin-bottom: 40px;
	}
	.blog-menu li {
	    display: inline-block;
	    margin-right: 10px;
	}
</style>
<script>
	export default {
		name : 'category',
		data : function(){
			return {
				category : [
					{
						name : 'Business',
						link : '#',
					},
					{
						name : 'Investing',
						link : '#',
					}
				]
			}
		},
		mounted : function(){
			console.log(this.category);
		}
	};
</script>