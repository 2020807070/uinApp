<template>
	<view class="pages">
		<view class="header">
			<uni-nav-bar left-icon="arrowleft" title="错题学习" @clickLeft="back" />
		</view>
		<view class="main"></view>
	</view>
</template>

<script>
	export default {
		methods: {
			back() {
				uni.navigateBack({
					delta: 1
				})
			},
		}
	}
</script>
<style>
	.pages {
		display: flex;
		flex-direction: column;
	}
	.main {
		flex: 1;
	}
</style>
