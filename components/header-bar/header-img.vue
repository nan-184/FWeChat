<template>
	<view>
		<image :style="getStyle" :src="src"></image>
	</view>
</template>
<script>
	export default{
		props:{
			size:{
				type:[String,Number],
				default:100
			},
			src:{
				type:String,
				default:''
			}
		},
		computed:{
			getStyle(){
				return `width: ${this.size}rpx;height: ${this.size}rpx;border-radius: 25rpx;`
			}
		}
	}
</script>
<style>
</style>
