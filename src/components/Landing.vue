<template>
	<div class="landing">
		<div class="landing__text">
			<h1>Arthur Marinheiro Vilela</h1>
			<h2>Desenvolvedor Web Full-stack</h2>
		</div>		
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component
export default class Landing extends Vue {

}
</script>

<style lang="scss">
@import "../assets/scss/_colors.scss";

.landing {
	background-color: $color-primary;
	width: 100%;
	height: 100vh;
	text-align: center;
	color: rgba($accent_text, 0.85);
	display: flex;
	justify-content: center;
	align-items: center;

	&__text {
		h1 {
			font-size: 4rem
		}
		h2 {
			font-size: 2rem
		}
	}
}
	
</style>