<template>
	<div>
		<div class="row">
			<div class="masthead masthead-blog" style="background-image:url('http://127.0.0.1/investree_invoice_squad/assets/uploader/blog/prev/ry4j-1485142370-logo-kompa.jpg')">
				<div class="masthead-blog-caption">
					<h3>Business</h3>
					<h1>Fix blog gann</h1>
					<div class="post-content-share">
						<div class="item"><i class="material-icons icon">visibility</i> 4</div>
					</div>
				</div>
			</div>
		</div>
		<isi-blog-component/>
	</div>
</template>
<style type="text/css">
	html, body {
	    height: 100%;
	}
	body {
	    padding: 0;
	    margin: 0;
	    font-family: "Open Sans", sans-serif;
	    font-weight: normal;
	    line-height: 1.5;
	    color: #666666;
	    background: #ffffff;
	    -webkit-font-smoothing: antialiased;
	    -moz-osx-font-smoothing: grayscale;
	}
	.row {
	    max-width: 75rem;
	    margin-left: auto;
	    margin-right: auto;
	}
	.masthead-blog:after {
	    content: '';
	    position: absolute;
	    top: 0;
	    left: 0;
	    background: rgba(0, 0, 0, 0.5);
	    height: 100%;
	}
	.masthead:after {
	    content: '';
	    width: 100%;
	    height: 60vh;
	    display: block;
	    position: absolute;
	    bottom: 0;
	    left: 0;
	    background: -moz-linear-gradient(top, transparent 0%, rgba(0, 0, 0, 0.65) 100%);
	    background: -webkit-linear-gradient(top, transparent 0%, rgba(0, 0, 0, 0.65) 100%);
	    background: linear-gradient(to bottom, transparent 0%, rgba(0, 0, 0, 0.65) 100%);
	    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00000000', endColorstr='#a6000000',GradientType=0 );
	}
	.masthead-blog .masthead-blog-caption {
	    position: absolute;
	    top: 50%;
	    left: 50%;
	    -moz-transform: translateX(-50%) translateY(-50%);
	    -webkit-transform: translateX(-50%) translateY(-50%);
	    transform: translateX(-50%) translateY(-50%);
	    width: 100%;
	    max-width: 1180px;
	    text-align: center;
	    color: white;
	    z-index: 10;
	}
	.fa {
		display: inline-block;
		font: normal normal normal 14px/1 FontAwesome;
		font-size: inherit;
		text-rendering: auto;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		transform: translate(0, 0);
	}
</style>
<script type="text/javascript">
	import IsiBlogComponent from '@/components/ViewBlog/IsiBlogComponent.vue';
	export default {
		name : 'view-blog-com',
		components : {
			IsiBlogComponent
		}
	};
</script>