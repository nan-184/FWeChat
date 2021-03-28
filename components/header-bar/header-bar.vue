<template>
	<!-- 导航栏 -->
	<view class="">
		<!--状态栏 -->
		<view :style="'height:'+statusBarHeight+'px'">
		</view>
		<!--  导航 -->
		<view class="tab-bav">
			<view class="tab-bav-cen">
				<slot></slot>
				
			</view>
			<!-- right -->
			<view class="tab-bav-right">
				<text class="iconfont">&#xe621;</text>
				<text class="iconfont">&#xe65c;</text>
			</view>


		</view>
	</view>
</template>

<script>
</script>

<style>
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
		font-weight:bold;
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
	.iconfont{
		font-size: 50rpx;
		padding: 0 10rpx;
	}
</style>
