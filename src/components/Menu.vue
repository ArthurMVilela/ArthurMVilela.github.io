<template>
	<nav class="menu">
		<div class="menu__topbar">
			<div class="menu__topbar__logotype">AMV</div>
			<div class="menu__topbar__links">
				<ul>
					<li v-for="link in links" :key="link.label">
						<a :href="link.link">{{ link.label }}</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

type MenuLink = {
	label: string;
	link: string;
};

@Component
export default class Menu extends Vue {
  links: MenuLink[] = [
  		{label: "Quem sou eu", link: "#who-am-i"},
  		{label: "Projetos", link: "#projects"},
  		{label: "Tecnologias", link: "#techs"}
  	]
}
</script>

<style lang="scss">
@import "../assets/scss/_colors.scss";

.menu {
	color: rgba($accent_text, 0.85);

	&__topbar {
		background-color: $color-primary-dark;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 60px;
		display: flex;
		justify-content: space-between;

		&__logotype {
			height: 60px;
			line-height: 60px;
			font-size: 2rem;
			font-weight: bold;
			padding: 0 1em;
		}

		&__links {
			ul {
				list-style: none;
				padding: 0;
				margin: 0;
			}

			li {
				display: inline-block;
				line-height: 60px;
				margin: 0 0.5em;
			}

			a {
				text-decoration: none;
  				font-weight: bold;
  				color: rgba($accent_text, 0.75);

  				&:hover {
  					color: rgba($accent_text, 0.85);
  				}
			}
		}
	}
}
</style>