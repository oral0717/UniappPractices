<template>
    <view>
        <match-media :min-width="375" :max-width="800" >
            <view>当页面最小宽度 375px， 页面宽度最大 800px 时显示</view>
        </match-media>

        <match-media :min-height="400" :orientation="portrait">
            <view>当页面高度不小于 400px 且屏幕方向为横向时展示这里</view>
        </match-media>
    </view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
