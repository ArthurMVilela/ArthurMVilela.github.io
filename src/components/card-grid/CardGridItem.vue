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
	margin: 10px;
	padding: 10px;
	box-shadow: 0px 10px 20px 5px rgba(0,0,0,0.15);
}

</style>