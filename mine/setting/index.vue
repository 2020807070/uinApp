<template>
	<view class="pages">
		<view class="header">
			<uni-nav-bar left-icon="arrowleft" title="设置" @clickLeft="back" />
		</view>
		<view class="main">
			<view></view>
			<view></view>
			<view></view>
			<view></view>
			<view></view>
			<view></view>
		</view>
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
		height: 100%;
		display: flex;
		flex-direction: column;
	}
	.header {
		
	}
	.main {
		flex: 1;
		height: 1208upx;
		background-color: rgb(238, 238, 238);
	}
</style>
