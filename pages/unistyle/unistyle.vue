<template>
	<view>
		<view>
			样式的学习
		</view>
		<view class="box1">
			测试文字
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	@import url("./a.scss");
	.box1{
		width:375rpx;
		height:375rpx;	
		font-size:30rpx;
		background:$global-color;
	}
</style>
