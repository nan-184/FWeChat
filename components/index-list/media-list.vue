<template>
	<view hover-class="bg-hover-light">
	<div @click="onClick" @longpress="long" class="contain" hover-class="bg-hover-light">
		 
	
		<!-- 左侧头像区 -->
		<view class="contain-left">
			<header-img :src="elem.img"></header-img>
			<!-- 微信角标 -->
			<corner-text v-if="elem.num" :num="elem.num">{{elem.num}}</corner-text>
	
		</view>
		<!-- 右侧信息区 -->
		<view class="contain-right">
			<view class="user-info">
				<text class="contain-right-use">{{elem.username}}</text>
				<text class="contain-right-info">{{elem.newinfo}}</text>
			</view>
			<text class="thetime">{{elem.thetime | formatTime}}</text>
		</view>
	</div>
	</view>
</template>

<script>
	//头像组件
	import headerImg from '@/components/header-bar/header-img.vue'
	//引入mixin时间格式化
	import freeBase from '@/common/mixin/free-base.js'
	//角标组件
	import cornerText from '@/components/header-bar/corner-text.vue'
	export default {
		mixins:[freeBase],
		components:{
			headerImg,
			cornerText
		},
		
		props:{
			elem:Object,
			index:Number
			
		},
		methods:{
			onClick(){
				this.$emit('click')
			},
			long(e){
				console.log(e)
			}
		}
	}
</script>

<style scoped>
	
	.contain {
		/* border: 1px solid #000; */
		width: 750rpx;
		height: 150rpx;
		margin-left: 25rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		/* justify-content: space-between; */
		/* #ifdef APP-PLUS-NVUE */
		margin: 0 13%;
		/* #endif */
		background-color: #FFFFFF;
	}
/* 	.contain:hover{
		background-color: #007AFF;
	} */
	
	.contain-left {
		/* position: relative; */
		/* width: 20%; */
		padding-top: 10rpx;
		/* border: 1px solid #000; */
		display: flex;
		width: 120rpx;
		flex-direction: row;
		align-content: stretch;
	}
	
	.contain-right {
		width: 545rpx;
		height: 130rpx;
		display: flex;
		right: -10rpx;
		flex-direction: row;
		justify-content: space-between;
		/* align-items: center; */
		/* padding-left:10px ; */
	
		border-bottom: 1px solid #ccc;
	}
	
	.user-info {
		width: 200rpx;
		display: flex;
		flex-direction: column;
		/* align-items: center; */
		justify-content: center;
		/* margin-left: 20rpx; */
	}
	
	.contain-right-use {
		font-size: 38rpx;
		/* font-weight: bold; */
	}
	
	.contain-right-info {
		font-size: 25rpx;
		color: #999999;
		/* overflow:hidden;
		text-overflow:ellipsis;
		white-space:nowrap;
		lines:1; */
	}
	
	.thetime {
		/* margin-right: 100rpx;
	width: 50rpx;
	height: 50rpx;
	background-color: #000000; */
		padding-top: 20rpx;
		font-size: 25rpx;
		color: #999999;
	}
	.bg-hover-light{ background-color: #dae0e5;}
</style>
