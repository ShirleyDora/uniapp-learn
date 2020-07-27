<template>
	<view>
		<view>
			导航跳转的学习
		</view>
		<!-- 声明式导航跳转跳转到TabBar页面需要加open-type -->
		<navigator url="/pages/detail/detail" open-type="switchTab">跳转至详情页</navigator>
		<navigator url="/pages/message/message?id=80&age=18">跳转至信息页</navigator>
		<navigator url="/pages/message/message" open-type="redirect">跳转至信息页</navigator>
		<!-- 编程式导航跳转 -->
		<button @click="goMessage">跳转至信息页</button>
		<button @click="goDetail">跳转至详情页</button>
		<button @click="redirectMessage">跳转到信息页并关闭当前页面</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		methods:{
			goMessage(){
				uni.navigateTo({
				    url: '/pages/message/message'
				});
			},
			goDetail(){
				uni.switchTab({
					url:'/pages/detail/detail'
				})
			},
			redirectMessage(){
				uni.redirectTo({
					url:'/pages/message/message'
				})
			}
		}
	}
</script>

<style lang="scss">

</style>
