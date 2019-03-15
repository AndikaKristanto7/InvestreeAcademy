<template>
	<div class="media-object media-object--article">
			<div class="media-object-section">
	    		<div class="thumbnail thumbnail--max">
			      <a :href="data.url"><img src="data.img" :alt="data.title"></a>
	    		</div>
	  		</div>
	 	<div class="media-object-section media-object-section--space">
		  	<div class="m-bottom-10">
			  	<small class="f-15 m-bottom-0">{{ data.category }}</small>
			    <h3 class="blue f-20 bold-blue m-top-0"><a :href="data.url">{{ data.title }}</a></h3>
		    </div>
		    <p>{{ data.words }}</p>
		    <a :href="data.url" class=" p-read-more theme-color"><p>Baca Selengkapnya</p>
		    <i class="icon-arrows_slim_right"></i></a>
		    <p><span class="author">{{ data.author }} — {{ data.post_date }}</span></p>
		    <p class="blog-meta"><i class="material-icons">View</i>&nbsp;<span>{{ data.view }}</span> <!-- <i class="material-icons">share</i> <span>200</span> --></p>
		</div>
	</div>
</template>
<style>
	.media-object {
		font-size: 15px;
		margin-bottom: 20px;
	}
	.media-object {
	    margin-bottom: 1rem;
	    display: block;
	}
	.media-object-section:first-child {
    	padding-right: 1rem;
	}
	.media-object-section {
	    display: table-cell;
	    vertical-align: top;
	}
	.media-object-section .thumbnail {
    	min-width: 111px;
	}
	.media-object .thumbnail {
	    position: relative;
	}

	.media-object-section > :last-child {
	    margin-bottom: 0;
	}
	.media-object--article .media-object-section .thumbnail img {
    	width: 266px;
	}
	.media-object img {
	    max-width: none;
	}
	@media screen and (min-width: 40em){
		.media-object-section--space {
			padding-left: 30px;
		}
	}
	.media-object-section {
	    display: table-cell;
	    vertical-align: top;
	}
</style>
<script>
	export default {
		name : 'blog-post',
		props : ['data'],		
	};
</script>