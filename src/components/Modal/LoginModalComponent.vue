<template>
	<div class="modal" :class="{ 'd-block' : isOpen }" tabindex="-1" role="dialog">
		<div class="modal-dialog modal-dialog-centered" role="document">
			<div class="modal-content">
		    	<div class="modal-header">
			        <h5 class="modal-title">Login</h5>
			        <button type="button" class="close" data-dismiss="modal" aria-label="Close" @click="closeModal">
			          <span aria-hidden="true">&times;</span>
			        </button>
			    </div>
				<div class="modal-body">
			        <form class="form-default" action="#" method="post" ajax-form="true">
			            <div class="row">
			            	<div class="col-md-12">
					            <div class="row">
					                <div class="col">
					                    <div class="info_modal"></div>
					                </div>
					            </div>
					            <div class="row"></div>
					            <div class="row">
					                <div class="col-md-3">
					                    <label for="middle-label" class="medium-text-right middle">Alamat Email*</label>
					                </div>
					                <div class="col-md-9">
					                    <input type="email" name="email" placeholder="Alamat Email" required="" class="form-control" >
					                </div>
					                <div class="m-bottom-10">
					                  <small class="red">Email invalid</small>
					                </div>   
					            </div>
					            <div class="row">
					                <div class="col-md-3">
					                    <label for="middle-label" class="medium-text-right middle">Password*</label>
					                </div>
					                <div class="col-md-9">
					                    <input type="password" name="password" placeholder="Password" required="" maxlength="120" class="form-control">
					                </div>
					            </div>
			      			</div>
						    <div class="modal-footer">
						        <button type="button" class="btn btn-primary">Save changes</button>
						        <button type="button" class="btn btn-secondary" data-dismiss="modal" @click="closeModal">Close</button>
					      	</div>
			    		</div>	
			    	</form>
				</div>
			</div>
		</div>
	</div>
</template>
<style type="text/css"></style>
<script type="text/javascript">
	export default {
		name : 'login-modal',
		props : ['isOpen'],
		methods : {
			closeModal : function(){
			    this.$emit("close-modal");
			},
		}
	};
</script>