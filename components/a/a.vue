<template>
	<view>
		这是A组件：<button @click="addNum">修改B组件数据</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		methods:{
			addNum(){
				uni.$emit('updateNum',10)
			}
		}
	}
</script>

<style lang="scss">

</style>
