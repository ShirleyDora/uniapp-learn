<template>
	<view id="myview">
		<!-- 这是test01组件{{num}} -->
		这是父组件传递来的数据{{title}}
		<button @click="sendNum">给父组件传值</button>
	</view>
</template>

<script>
	export default {
		// data() {
		// 	return {
		// 		num:3,
		// 		intId:null
		// 	};
		// },
		// beforeCreate(){
		// 	console.log('实例已经开始初始化了')
		// 	console.log(this.num)
		// },
		// created(){
		// 	console.log('created',this.num);
		// 	this.intId=setInterval(()=>{
		// 		console.log('执行定时器')
		// 	},1000)
		// },//一般初始化数据
		// beforeMount(){
		// 	console.log('beforeMount',document.getElementById("myview"))
		// },
		// mounted(){
		// 	console.log('mounted',document.getElementById("myview"))
		// },//一般操作DOM
		// destroyed(){
		// 	console.log('组件销毁了');
		// 	clearInterval(this.intId)
		// }
		props:['title'],
		data(){
			return{
				num:3
			}
		},
		methods:{
			sendNum(){
				// console.log('给父亲传值');
				this.$emit('myEven',this.num)
			}
		}
	}
</script>

<style lang="scss">

</style>
