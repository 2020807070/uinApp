<template>
	<view class="pages">
		<cover-view class="header" :style="headStyle">
			<image class="header-icon" src="../../static/home/more.png" mode=""></image>
			<cover-view class="header-text">设置</cover-view>
		</cover-view>
		<view class="main" :style="mainStyle">
			<view>000</view>
			<view>000</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
			<view>123</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				top: 0,
				height: 0
			}
		},
		computed: {
			headStyle() {
				console.log(this.top)
				return 'padding-top: ' + this.top * 2 + 'rpx;line-height:' + this.height * 2 + 'rpx';
			},
			mainStyle() {
				return 'margin-top: ' + this.top * 2 + 'rpx';
			}
		},
		mounted() {
				try {
					this.top = wx.getMenuButtonBoundingClientRect().top;
					this.height = wx.getMenuButtonBoundingClientRect().height;
				} catch {
					this.top = 20;
					this.height = 48;
				}

		},
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
	.header {
		position: fixed;
		width: 100%;
		top: 0;
		left: 0;
		display: flex;
		align-items: center;
		z-index: 999;
		height: 80upx;
		background-color: #FFFFFF;
	}

	.header-icon {
		margin-left: 17upx;
		width: 17upx;
		height: 32upx;
		transform: scale(-1, -1);
	}

	.header-text {
		position: absolute;
		left: 50%;
		transform: translateX(-50%);
		font-size: 36upx;
	}

	.pages {
		height: 100%;
		display: flex;
		flex-direction: column;
	}

	.header {}

	.main {
		flex: 1;
		height: 1208upx;
		background-color: rgb(238, 238, 238);
	}
</style>
