<template>
	<a v-if="link" :href="url" class="button"><slot></slot></a>
	<button v-else class="button"><slot></slot></button>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Button extends Vue {
	@Prop({default: false}) link!: boolean;
	@Prop({default: "#"}) url!: string;
}
</script>

<style lang="scss">
@import "../assets/scss/_colors.scss";

.button {
	background: none;
	border: none;
	display: inline-block;
	text-decoration: none;
	color: $color-secondary;
	font-weight: bold;
	padding: 0.5em 1em;
	border-radius: 5px;
	transition: background-color 300ms, box-shadow 300ms;
	font-size: 1rem;
	cursor: pointer;

	&:hover {
		background-color: rgba($color-secondary, 0.15)
	}

	&--outlined {
		border: solid 2px $color-secondary;
	}

	&--contained {
		background-color: $color-secondary;
		-webkit-box-shadow: 0px 5px 5px 2px rgba(0,0,0,0.2); 
		box-shadow: 0px 5px 5px 2px rgba(0,0,0,0.2);
		color: white;

		&:hover {
			background-color: $color-secondary;
			-webkit-box-shadow: 0px 7px 5px 2px rgba(0,0,0,0.15); 
			box-shadow: 0px 7px 5px 2px rgba(0,0,0,0.15);
		}
	}


}
</style>