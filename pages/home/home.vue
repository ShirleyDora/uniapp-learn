<template>
	<view>
		<view class="">
			数据绑定的学习
		</view>
		<view>
			{{msg}}
		</view>
		<view>{{1+'你好'}}</view>
		<view>{{1+1}}</view>
		<view>{{flag?'这是反话-我是假的':'这是反话-我是真的'}}</view>
		<image v-bind:src="imgUrl" alt="">
		<image :src="imgUrl" alt="">
		<view v-for="(item,index) in arr" :key="item.id">
			序号：{{item.id}}
			名字：{{item.name}}
			年龄：{{item.age}}
		</view>
		<button type="primary" v-on:click="clickButton">按钮</button>
		<button type="primary" @click="clickButton">按钮</button>
		<button type="primary" @click="clickButton(20,$event)">按钮</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg:'hello',
				flag:false,
				imgUrl:'http://destiny001.gitee.io/image/monkey_02.jpg',
				arr:[
					{
						name:'可可',
						age:20,
						id:1
					},
					{
						name:'爱爱',
						age:18,
						id:2
					},
					{
						name:'没有',
						age:20,
						id:3
					},
					{
						name:'脑袋',
						age:18,
						id:4
					},
				]
			};
		},
		methods:{
			clickButton(num,e){
				console.log('点击我了',num,e)
			}
		}
	}
</script>

<style lang="scss">

</style>
