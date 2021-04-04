<template>
	<!-- 导航栏 -->
	<view class="content">
		<!--状态栏 -->
		<view  class="status-bar" :style="{'height':statusBarHeight+'px'}" style="background-color:#ededed ;">
		</view>
		<!-- <view>12345</view> -->
		<!--  导航 -->
		<view class="tab-bav">
			<view class="tab-bav-cen">
				<slot></slot>
			</view>
			<!-- right -->
			<view class="tab-bav-right">
				<view class="iconfont">
					<slot name="glass"></slot>
				</view>
				<view class="iconfont">
					<slot name="add"></slot>
				</view>
			</view>


		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				statusBarHeight: 0
			}
		},
		mounted() {
			// #ifdef APP-PLUS-NVUE
			this.statusBarHeight = plus.navigator.getStatusbarHeight();
			// #endif
			this.navBarHeight=this.statusBarHeight+uni.upx2px(90)
				},
	}
</script>

<style lang="scss">
	.content {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 10;
	}
	.tab-bav {
		width: 750rpx;
		height: 90rpx;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		background-color: #ededed;
	}

	.tab-bav-cen {
		font-weight: bold;
	}

	.tab-bav-right {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		position: fixed;
		margin-right: 20rpx;
		right: 0;
	}

	.iconfont {
		font-size: 50rpx;
		padding: 0 10rpx;
	}
</style>
