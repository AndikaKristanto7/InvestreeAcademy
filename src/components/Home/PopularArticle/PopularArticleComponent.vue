<template>
	<div>
		<h3 class="f-20 bold blue">Artikel Terpopuler</h3>
		<hr class="m-top-20 m-bottom-20">
		<ul class="f-14 m-bottom-30">
		    <li v-for="data in populars">
	        	<a :href="data.url">{{ data.title }}</a>
	       	</li>
		</ul>
		<h3 class="f-20 bold blue">Tags</h3>
		<hr class="m-top-20 m-bottom-20">
		<div class="widget-tags">
	    	<a v-for="tag in tags" :href="tag.url">{{ tag.title }}</a>
	    </div>
	</div>
</template>
<style type="text/css">
	a {
	    color: #154276;
	    text-decoration: none;
	    line-height: inherit;
	    cursor: pointer;
	}

	a {
	    background-color: transparent;
	}
	.widget-tags a {
	    font-size: 13px;
	    display: inline-block;
	    margin-bottom: 10px;
	    padding: 3px 10px;
	    color: #123F74;
	    border: 1px solid #d3d3d3;
	    border-radius: 50px;
	}

</style>
<script type="text/javascript">
	export default {
		name : 'popular-article-comp',
		props : ['populars','tags'],
	};
</script>