<template>
	<view :style="{background:color,fontSize: '26px'}"
		@click="handleClick"
	>
		card<slot></slot>
	</view>
</template>

<script>
	export default {
		name:"card",
		props: {
			color: {
				type: String,
				default: 'yellow'
			},
		},
		data() {
			return {
				
			};
		},
		methods: {
			handleClick(){
				console.log('子组件')
				this.$emit('myClick', {a: 11}, {b:22})
			}
		}
	}
</script>

<style>

</style>