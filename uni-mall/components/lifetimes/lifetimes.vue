<template>
	<view>
		<slot v-if="flag"></slot>
		<button @click="change">点击update</button>
	</view>
</template>

<script>
	export default {
		name:"lifetimes",
		data() {
			return {
				flag:false
			};
		},
		beforeCreate() {
			console.log('comp beforeCreate')
		},
		created() {
			console.log('comp created')
		},
		beforeMount() {
			console.log('comp beforeMount')
		},
		mounted() {
			console.log('comp mounted')
		},
		beforeUpdate() {
			console.log('comp beforeUpdate')
		},
		updated() {
			console.log('comp updated')
		},
		// beforeUnmount() {
		// 	console.log('comp feforeUnmount')
		// },
		// unmounted() {
		// 	console.log('comp unmounted')
		// },
		beforeDestroy() {
			console.log('comp beforeDestroy')
		},
		destroyed() {
			console.log('comp destroyed')
		},
		methods: {
			change() {
				console.log(1)
				this.flag=!this.flag
				console.log(2)
			}
		}
	}
</script>

<style>

</style>