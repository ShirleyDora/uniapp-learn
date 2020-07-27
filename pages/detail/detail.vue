<template>
	<view>
		<view>
			<text>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text selectable>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="ensp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="emsp">唱歌 跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="emsp" style="font-size: 30px;">唱歌 跳舞打篮球</text>
		</view>
		<view>
			<text>&amp;</text>
		</view>
		<!--  #ifdef H5 -->
		<view>我希望在h5中显示</view>
		<!--  #endif -->
		<!--  #ifdef MP-WEIXIN -->
		<view>我希望在微信小程序中显示</view>
		<!--  #endif -->
		<view>
			<button type="primary" @click="chooseImg">上传图片</button>
			<image v-for="(item,index) in imgArr" :src="item" :key="index" @click="previewImg(item)"></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgArr:[]
			};
		},
		methods:{
			chooseImg(){
				uni.chooseImage({
				    count: 6, //上传了6张
				   	success:res=>{
						//上传图片成功后
						this.imgArr = res.tempFilePaths;
				    }
				});
			},
			previewImg(current){
				console.log(current)
				uni.previewImage({
					current,
					urls:this.imgArr,
					loop:true,
					indicator:'default'
				})
			}
		}
	,
	onLoad(){
		// #ifdef H5
		console.log('我希望h5打印')
		// #endif
		// #ifdef MP-WEIXIN
		console.log('我希望微信小程序中打印')
		// #endif
	}
	}
</script>

<style lang="scss">
	/* #ifdef H5 */
	view{
		color:hotpink;
	}
	/* #endif */
	/* #ifdef MP-WEIXIN */
	view{
		color:#0000FF;
	}
	/* #endif */
	
</style>
