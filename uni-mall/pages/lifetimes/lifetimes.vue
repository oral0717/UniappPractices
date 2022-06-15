<template>
	<view>
		生命周期页面
		<button @click="change">点击我</button>
		<lifetimes v-if="flag">生命周期组件</lifetimes>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				flag:true
			}
		},
		onLoad() {
			console.log('page onLoad')
		},
		onShow() {
			console.log('page onShow')
		},
		onReady() {
			console.log('page onReady')
		},
		onHide() {
			console.log('page onHide')
		},
		onUnload() {
			console.log('page onUnload')
		},
		onResize(){
			console.log('page onResize')
		},
		methods:{
			change(){
				this.flag=!this.flag
			}
		}
	}
</script>

<style>

</style>
