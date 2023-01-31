<template>
	<section class="app-sidebar">
		<nav class="sidebar sidebar-offcanvas" id="sidebar">
			<ul class="nav">
				<li class="nav-item">
					<a class="nav-link">
						<i class="menu-icon typcn typcn-document-text"></i>
						<router-link class="menu-title" to="/">Dashboard</router-link>
					</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" v-b-toggle="'ui-basic'">
						<i class="menu-icon typcn typcn-coffee"></i>
						<span class="menu-title">Basic UI Elements</span>
						<i class="menu-arrow"></i>
					</a>
					<b-collapse id="ui-basic">
						<ul class="nav flex-column sub-menu">
							<li class="nav-item">
								<router-link class="nav-link" to="/buttons/">Buttons</router-link>
							</li>
							<li class="nav-item">
								<router-link class="nav-link" to="/dropdowns/">Dropdowns</router-link>
							</li>
							<li class="nav-item">
								<router-link class="nav-link" to="/typography/">Typography</router-link>
							</li>
						</ul>
					</b-collapse>
				</li>
				<li class="nav-item">
					<span class="nav-link" v-b-toggle="'charts-dropdown'">
						<i class="menu-icon typcn typcn-th-large-outline"></i>
						<span class="menu-title">Charts</span>
						<i class="menu-arrow"></i>
					</span>
					<b-collapse id="charts-dropdown">
						<ul class="nav flex-column sub-menu">
							<li class="nav-item">
								<router-link class="nav-link" to="/chartjs/">Chart js</router-link>
							</li>
						</ul>
					</b-collapse>
				</li>
				<li class="nav-item">
					<a class="nav-link" v-b-toggle="'tables'">
						<i class="menu-icon mdi mdi-table"></i>
						<span class="menu-title">Tables</span>
						<i class="menu-arrow"></i>
					</a>
					<b-collapse id="tables">
						<ul class="nav flex-column sub-menu">
							<li class="nav-item">
								<router-link class="nav-link" to="/basic_table/">Basic Table</router-link>
							</li>
						</ul>
					</b-collapse>
				</li>
				<li class="nav-item">
					<a class="nav-link" v-b-toggle="'icons'">
						<i class="menu-icon typcn typcn-user-outline"></i>
						<span class="menu-title">Icons</span>
						<i class="menu-arrow"></i>
					</a>
					<b-collapse id="icons">
						<ul class="nav flex-column sub-menu">
							<li class="nav-item">
								<router-link class="nav-link" to="/mdiIcons/">MDI</router-link>
							</li>
						</ul>
					</b-collapse>
				</li>
			</ul>
		</nav>
	</section>
</template>

<script>
import JQuery from 'jquery'
// eslint-disable-next-line
let $ = JQuery
export default {
	name: 'app-sidebar',
	mounted () {
		const body = document.querySelector('body')
		// add class 'hover-open' to sidebar navitem while hover in sidebar-icon-only menu
		document.querySelectorAll('.sidebar .nav-item').forEach(function (el) {
			el.addEventListener('mouseover', function () {
				if (body.classList.contains('sidebar-icon-only')) {
					el.classList.add('hover-open')
				}
			})
			el.addEventListener('mouseout', function () {
				if (body.classList.contains('sidebar-icon-only')) {
					el.classList.remove('hover-open')
				}
			})
		})
	}
}
</script>
