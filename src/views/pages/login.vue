<template>
	<section class="login">
		<div class="container-scroller">
			<div class="container-fluid page-body-wrapper full-page-wrapper">
				<div class="content-wrapper d-flex align-items-center auth auth-bg-1 theme-one">
					<div class="row w-100">
						<div class="col-lg-4 mx-auto">
							<div class="auto-form-wrapper">
								<form action="#">
									<div class="form-group">
										<label class="label">Username</label>
										<div class="input-group">
											<input type="text" class="form-control" placeholder="Username">
											<div class="input-group-append">
												<span class="input-group-text">
													<i class="mdi mdi-check-circle-outline"></i>
												</span>
											</div>
										</div>
									</div>
									<div class="form-group">
										<label class="label">Password</label>
										<div class="input-group">
											<input type="password" class="form-control" placeholder="*********">
											<div class="input-group-append">
												<span class="input-group-text">
													<i class="mdi mdi-check-circle-outline"></i>
												</span>
											</div>
										</div>
									</div>
									<div class="form-group">
										<button class="btn btn-primary submit-btn btn-block">Login</button>
									</div>
									<div class="form-group d-flex justify-content-between">
										<div class="form-check form-check-flat mt-0">
											<label class="form-check-label">
												<input type="checkbox" class="form-check-input" checked> Keep me signed in
											</label>
										</div>
										<a href="#" class="text-small forgot-password text-black">Forgot Password</a>
									</div>
									<div class="text-block text-center my-3">
										<span class="text-small font-weight-semibold">Not a member ?</span>
										<router-link to="/register" class="text-black text-small">Create new account</router-link>
									</div>
								</form>
							</div>
							<p class="footer-text text-center">copyright © 2023 V88. All rights reserved.</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
<script>
export default {
	name: 'login'
}
</script>
