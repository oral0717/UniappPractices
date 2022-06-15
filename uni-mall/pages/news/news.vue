<template>
	<view>
		<card color="red">red</card>
		<card color="blue">blue</card>
		<card :color="color" @myClick="myClick">{{color}}</card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				color: 'pink'
			}
		},
		methods: {
			myClick(...rest){
				console.log('父组件', rest)
			}
		}
	}
</script>

<style>

</style>
