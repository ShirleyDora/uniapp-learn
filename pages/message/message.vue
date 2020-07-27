<template>
	<view>
		<view class="box2" hover-class="box2-active">
			<view class="box" :hover-start-time="2000" :hover-stay-time="2000" hover-class="box-active" hover-stop-propagation>我是一个大盒子</view>
		</view>
		<button>按钮</button>
		<button size="mini">普通按钮</button>
		<button type="primary">小按钮</button>
		<button size="primary" plain>镂空按钮</button>
		<button size="primary" disabled>禁用按钮</button>
		<button loading>加载按钮</button>
		<image src="http://destiny001.gitee.io/image/cxk.gif"></image>
		<image src="http://destiny001.gitee.io/image/cxk.gif" mode="aspectFit"></image><!-- 保持长边缩放，一般用这个 -->
		<image src="http://destiny001.gitee.io/image/cxk.gif" mode="aspectFill"></image><!-- 保持短边缩放 -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		onLoad(options){
			console.log(options)
		}
	}
</script>

<style lang="scss">
	.box{
		width:100px;
		height:100px;
		background:green;
		
	}
	.box-active{
		background:pink;
	}
	.box2{
		width:200px;
		height:200px;
		background:blue;
	}	
	.box2-active{
		background:yellow;
	}
	
</style>
