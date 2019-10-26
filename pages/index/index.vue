<template>
	<view class="content">
		<view :class="starClass" @click="star"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				starClass: "fave",
			}
		},
		onLoad() {


		},
		methods: {
			star() {
				this.starClass += " active";
			}

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.fave {
		background: url(../../static/twitter_fave.png) no-repeat;
		background-position: 0 0;
		width: 70px;
		height: 50px;
		cursor: pointer;
	}

	.fave.active {
		background-position: -3519px 0;
		transition: background 8s steps(55);
	}
</style>
