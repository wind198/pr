<template>
	<div>
		<b-navbar id="template-header" class="navbar default-layout col-lg-12 col-12 p-0 d-flex flex-row" toggleable="md">
			<div class="text-center navbar-brand-wrapper d-flex align-items-top justify-content-center">
				<router-link class="navbar-brand brand-logo" to="/">
					<img src="@/assets/images/logo-daibet.png" alt="logo" />
				</router-link>
				<router-link class="navbar-brand brand-logo-mini" to="/">
					<img src="@/assets/images/icons/icon36.png" alt="logo" />
				</router-link>
			</div>
			<div class="navbar-menu-wrapper d-flex align-items-center ml-auto ml-lg-0">
				<button class="navbar-toggler navbar-toggler align-self-center" type="button" @click="collapedSidebar()">
					<span class="mdi mdi-menu"></span>
				</button>
				<b-navbar-nav class="navbar-nav-right ml-auto">
					<b-nav-item-dropdown right class="preview-list">
						<template slot="button-content">
							<div class="nav-link count-indicator">
								<i class="mdi mdi-bell-outline"></i>
								<span class="count">7</span>
							</div>
						</template>
						<b-dropdown-item class="preview-item py-2 px-0 border-bottom">
							<p class="mb-0 font-weight-medium float-left">You have 7 unread mails </p>
							<span class="badge badge-pill badge-primary float-right">View all</span>
						</b-dropdown-item>
						<b-dropdown-item class="preview-item">
							<div class="preview-thumbnail">
								<img src="@/assets/images/faces/face2.jpg" alt="image" class="img-sm profile-pic">
							</div>
							<div class="preview-item-content flex-grow py-2">
								<p class="preview-subject ellipsis font-weight-medium text-dark">Travis Jenkins</p>
								<p class="font-weight-light small-text"> The meeting is cancelled </p>
							</div>
						</b-dropdown-item>
					</b-nav-item-dropdown>
					<b-nav-item-dropdown right class="preview-list">
						<template slot="button-content">
							<div class="nav-link count-indicator">
								<i class="mdi mdi-email-outline"></i>
								<span class="count bg-success">4</span>
							</div>
						</template>
						<b-dropdown-item class="preview-item py-2 px-0 border-bottom">
							<p class="mb-0 font-weight-medium float-left">You have 4 new notifications </p>
							<span class="badge badge-pill badge-primary ml-auto">View all</span>
						</b-dropdown-item>
						<b-dropdown-item class="preview-item">
							<div class="preview-thumbnail">
								<i class="mdi mdi-alert m-auto text-primary"></i>
							</div>
							<div class="preview-item-content flex-grow py-2">
								<h6 class="preview-subject font-weight-normal text-dark mb-1">Application Error</h6>
								<p class="font-weight-light small-text mb-0"> Just now </p>
							</div>
						</b-dropdown-item>
						<b-dropdown-item class="preview-item">
							<div class="preview-thumbnail">
								<i class="mdi mdi-airballoon m-auto text-primary"></i>
							</div>
							<div class="preview-item-content flex-grow py-2">
								<h6 class="preview-subject font-weight-normal text-dark mb-1">New user registration</h6>
								<p class="font-weight-light small-text mb-0"> 2 days ago </p>
							</div>
						</b-dropdown-item>
					</b-nav-item-dropdown>
					<b-nav-item-dropdown right class="preview-list user-dropdown">
						<template slot="button-content">
							<div class="d-flex align-items-center">
								<img class="img-xs rounded-circle" src="@/assets/images/faces/face1.jpg" alt="Profile image">
							</div>
						</template>
						<b-dropdown-item>
							<div class="dropdown-header text-center w-100">
								<img class="img-md rounded-circle" src="@/assets/images/faces/face1.jpg" alt="Profile image">
								<p class="mb-1 mt-3 font-weight-semibold">Allen Moreno</p>
								<p class="font-weight-light text-muted mb-0">allenmoreno@gmail.com</p>
							</div>
						</b-dropdown-item>
						<b-dropdown-item>My Profile <span class="badge badge-pill badge-danger">1</span><i class="dropdown-item-icon ti-dashboard"></i></b-dropdown-item>
						<b-dropdown-item>Sign Out<i class="dropdown-item-icon ti-power-off"></i></b-dropdown-item>
					</b-nav-item-dropdown>
				</b-navbar-nav>
				<button class="navbar-toggler navbar-toggler-right align-self-center" type="button" @click="collapedMobileSidebar()">
					<span class="mdi mdi-menu"></span>
				</button>
			</div>
		</b-navbar>
	</div>
</template>

<script lang="js">
import JQuery from 'jquery'
let $ = JQuery
export default {
	name: 'app-header',
	methods: {
		collapedSidebar: function () {
			$('body').toggleClass('sidebar-icon-only')
		},
		collapedMobileSidebar: function () {
			$('#sidebar').toggleClass('active')
		}
	}
}
</script>
