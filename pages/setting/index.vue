<template>
	<view class="setting">
		<view class="setting-mian">
			<view class="setting-item" style="margin-top: 30upx">
				<view>头像</view>
				<image class="head" src="../../static/nav/match.png" mode=""></image>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="setting-item">
				<view>昵称</view>
				<view>大妮子</view>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="setting-item">
				<view>电话</view>
				<view>12345678944</view>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="setting-item">
				<view>性别</view>
				<view>女</view>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="setting-item">
				<view>身份证号</view>
				<view>578451236987451254</view>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="setting-item">
				<view>居住地址</view>
				<view>海南白沙县农场大大</view>
				<image class="icon" src="../../static/home/more.png" mode=""></image>
			</view>
		</view>
		
		<view class="setting-btn">
			退出当前登录
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
	}
</script>
<style>
	.setting {
		height: 94vh;
		background-color: rgb(238, 238, 238);
		overflow: hidden;
	}
	
	.setting-btn {
		text-align: center;
		line-height: 80upx;
		letter-spacing: 5upx;
		color: rgba(0, 0, 0, .8);
		background-color: #FFFFFF;
		width: 100%;
		margin-top: 30upx;
		font-size: 30upx;
		height: 80upx;
	}
	
	.setting-mian {
		overflow: hidden;
		margin-top: 30upx;
	}
	
	.setting-item {
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #FFFFFF;
		border-bottom: 1upx solid rgba(0, 0, 0, .1);
		padding: 26upx 30upx;
		font-size: 26upx;
		color: rgba(0, 0, 0, .7);
		padding-right: 50upx;
	}
	
	.setting-item .icon {
		position: absolute;
		right: 15upx;
		width: 17upx;
		height: 32upx;
	}
	
	.head {
		width: 80upx;
		height: 80upx;
	}
</style>
