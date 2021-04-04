<template>

	<view class="my-badge">
		<text style="color: #FFFFFF;font-size: 25upx;">{{num}}</text>
	</view>
</template>

<script>
	export default {
		props: {
			num: {
				type: [Number, String],
				default: ''
			}
		}
	}
</script>

<style>
	.my-badge {
		position: relative;
		top: -10rpx;
		right: 30upx;
		width: 40rpx;
		height: 40rpx;
		background-color: #ff0000;
		border-radius: 20rpx;
		/* 		text-align: center;
		font-size: 30rpx; */
		/* color: #fff; */
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 10rpx;
		color: #FFFFFF;
	}

	/* .corner {
		position: relative;
		top: -10rpx;
		left: -20rpx;
		width: 40rpx;
		height: 40rpx;
		background-color: #ff0000;
		border-radius: 20rpx;
		text-align: center;
		font-size: 30rpx;
		color: #fff;
	} */
</style>
