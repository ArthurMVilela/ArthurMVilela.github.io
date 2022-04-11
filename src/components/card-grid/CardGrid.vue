<template>
	<div class="card-grid">
		<slot></slot>
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class CardGrid extends Vue {

}
</script>

<style lang="scss">
.card-grid {
	display: grid;
	width: 100%;
	grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
	grid-template-rows: 1fr;
}
</style>