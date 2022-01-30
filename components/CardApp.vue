<script lang="ts" setup>
import { Motion, Presence } from "motion/vue";
</script>

<template>
	<Motion
		:initial="{ opacity: 0, scale: 0 }"
		:animate="{ opacity: 1, scale: 1 }"
	>
		<div class="card">
			<div class="card-body">
				<div class="card-img">
					<img src="~/assets/images/logo.png" />
				</div>
				<div class="card-text">
					<p>Add</p>
					<span>The Founder</span>
				</div>
			</div>
		</div>
	</Motion>
</template>

<style lang="scss" scoped>
.card {
	align-items: center;
	background-color: #333;
	display: flex;
	justify-content: center;
	margin: 10px;

	.card-body {
		align-items: center;
		background-color: #fff;
		border-radius: 10px;
		display: flex;
		flex-direction: column;
		height: 200px;
		justify-content: center;
		width: 200px;

		.card-img {
			border: 1px solid #1e1e1e;
			border-radius: 100%;
			margin-bottom: 24px;
			max-height: 80px;
			max-width: 80px;
			img {
				height: 100%;
				width: 100%;
			}
		}

		.card-text {
			text-align: center;
		}
	}
}
</style>
