<template>
	<footer class="footer">
		<div class="footer__content">
			<div class="footer__links">
				<a href="">Github</a>
				<a href="">Linkedin</a>
			</div>
		</div>
	</footer>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component
export default class Footer extends Vue {

}
</script>

<style lang="scss">
@import "../assets/scss/_colors.scss";
	
.footer {
	width: 100%;
	min-height: 200px;
	background-color: $color-primary-dark;
	color: white;

	&__content {
		width: 100%;
		max-width: 1020px;
		margin: 0 auto;
		display: flex;
		align-items: center;
	}

	&__links {

	}
}
</style>