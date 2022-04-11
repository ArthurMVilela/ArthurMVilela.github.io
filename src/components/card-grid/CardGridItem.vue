<template>
	<div class="card-grid__item">
		<slot></slot>
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class CardGridItem extends Vue {

}
</script>

<style lang="scss">

.card-grid__item {
	background: white;
	border-radius: 5px;
	padding: 10px;
	-webkit-box-shadow: 0px 5px 5px 2px rgba(0,0,0,0.2); 
	box-shadow: 0px 5px 5px 2px rgba(0,0,0,0.2);

	&--span-2 {
		grid-column: span 2;

	}
}

</style>