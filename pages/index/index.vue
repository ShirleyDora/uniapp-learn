<template>
	<view class="container">
		<!-- <view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<text class="intro">详见：</text>
		<uni-link :href="href" :text="href"></uni-link> -->
		<test01 v-if="flag" :title="title" @myEven="getNum"></test01>
		<button type="primary" @click="checkTest">切换test01组件</button>
		这是子组件传递来的数据{{num}}
		<testA></testA>
		<testB></testB>
		<view>
		    <uni-calendar 
		    :insert="true"
		    :lunar="true" 
		    :start-date="'2020-3-2'"
		    :end-date="'2020-5-20'"
		    @change="change"
		     />
		</view>
	</view>
</template>

<script>
	import test01 from '../../components/test01/test01.vue';
	import testA from '../../components/a/a.vue';
	import testB from '../../components/b/b.vue';
	
	import uniCalendar from '@/components/uni-calendar/uni-calendar.vue'
	export default {
		data(){
			return{
				title:'hello',
				flag:true,
				num:0
			}
		},
		methods:{
			checkTest(){
				this.flag=!this.flag;
			},
			getNum(num){
				// console.log(num);
				this.num=num;
			},
			 change(e) {
			            console.log(e);
			        }
		},
		// data() {
		// 	return {
		// 		href: 'https://uniapp.dcloud.io/component/README?id=uniui'
		// 	}
		// },
		// onLoad(options){
		// 	console.log('页面加载了',options);
		// },
		// onShow(){
		// 	console.log('页面显示了')
		// },
		// onReady(){
		// 	console.log('页面初次渲染完成了')
		// },
		// onHide(){
		// 	console.log('页面隐藏了')
		// },
		// methods: {

		// },
		components:{
			test01,
			testA,
			testB,
			uniCalendar
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
