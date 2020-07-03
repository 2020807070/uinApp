<template>
	<view>
		<view class="list">
			<view class="user-wrap">
				<view class="user-title">
					<image class="logo" src="../../static/common/logo.png" mode=""></image>
					<view class="title">个人中心</view>
				</view>
				<view class="user-info">
					<image class="user-head" src="../../static/nav/match-a.png" mode=""></image>
					<view class="user-name">甲乙丙丁</view>
					<view class="setting" @click="goPage('setting')">
						<image class="setting-icon" src="../../static/mine/setting.png"></image>
						<view class="setting-text">设置</view>
					</view>
					<view class="count" @click="goPage('rank')">
						<view class="count-num">10</view>积分
					</view>
				</view>
			</view>
			<view class="list-item" @click="goPage('record')">
				<view class="list-item-icon">
					<image src="../../static/mine/record.png" mode="" style="width: 36upx;height: 42upx;"></image>
				</view>
				<view class="list-item-text">答题记录</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('search')">
				<view class="list-item-icon">
					<image src="../../static/mine/search.png" mode="" style="width: 34upx;height: 34upx;"></image>
				</view>
				<view class="list-item-text">错题查询</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('study')">
				<view class="list-item-icon">
					<image src="../../static/mine/study_history.png" mode="" style="width: 40upx;height: 40upx;"></image>
				</view>
				<view class="list-item-text">学习记录</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('sign')">
				<view class="list-item-icon">
					<image src="../../static/mine/sign.png" mode="" style="width: 36upx;height: 42upx;"></image>
				</view>
				<view class="list-item-text">标记题目</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('record')">
				<view class="list-item-icon">
					<image src="../../static/mine/collection.png" mode="" style="width: 40upx;height: 32upx;"></image>
				</view>
				<view class="list-item-text">收藏</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('center')">
				<view class="list-item-icon">
					<image src="../../static/mine/integral.png" mode="" style="width: 34upx;height: 36upx;"></image>
				</view>
				<view class="list-item-text">积分历史</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>

			<view class="list-item"  @click="goPage('proposal')">
				<view class="list-item-icon">
					<image src="../../static/mine/service.png" mode="" style="width: 34upx;height: 34upx;"></image>
				</view>
				<view class="list-item-text">在线咨询</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
			<view class="list-item"  @click="goPage('proposal')">
				<view class="list-item-icon">
					<image src="../../static/mine/history.png" mode="" style="width: 30upx;height: 30upx;"></image>
				</view>
				<view class="list-item-text">建议</view>
				<image class="list-item-arrow" src="../../static/home/more.png" mode=""></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				top: 48,
			}
		},
		mounted () {
			// this.top = wx.getMenuButtonBoundingClientRect().top;
			console.log(wx.getMenuButtonBoundingClientRect());
		},
		methods: {
			goPage (path) {
				uni.navigateTo({
					url: `/pages/${path}/index`
				});
			}
		}
	}
	
</script>

<style>


	.user-wrap {
		position: relative;
		height: 182upx; // 202
		background-color: rgb(37, 163, 203);
		margin-bottom: 184upx;
	}

	.user-title {
		position: relative;
	}
	
	.logo {
		position: absolute;
		top: 66upx;
		width: 122upx;
		height: 36upx;
		left: 20upx;
	}
	
	.title {
		position: absolute;
		top: 66upx;
		left: 50%;
		transform: translateX(-50%);
		color: #fff;
		font-size: 30upx;
	}

	.user-head {
		margin-top: 35upx;
		margin-left: 35upx;
		width: 114upx;
		height: 114upx;
		border-radius: 50%;
	}
	
	.user-name {
		position: absolute;
		font-size: 19px;
		top: 65upx;
		left: 168upx;
	}
	
	.setting {
		display: flex;
		position: absolute;
		top: 21upx;
		right: 24upx;
		align-items: center;
	}
	.setting-icon {
		margin-right: 11upx;
		width: 34upx;
		height: 34upx;
	}
	
	.setting-text {
		font-size: 14px;
	}
	
	.count {
		display: flex;
		position: absolute;
		bottom: 20upx;
		right: 24upx;
		font-size: 30upx;
		color: #c00000;
		align-items: flex-end;
	}
	
	.count-num {
		margin-right: 10upx;
		font-size: 50upx;
	}
	
	.list-item {
		position: relative;
		width: 696upx;
		margin: 0 30upx;
		margin-top: 40upx;
		padding-bottom: 16upx;
		font-size: 26upx;
		color: #1a1a1a;
		display: flex;
		border-bottom: 2upx solid rgba(0, 0, 0, .1);
	}

	.list-item-icon {
		text-align: center;
		width: 36upx;
		height: 42upx;
		margin-right: 16upx;
	}

	.list-item-arrow {
		position: absolute;
		right: 10upx;
		width: 16upx;
		height: 30upx;
	}

	.user-info {
		position: absolute;
		top: 144upx; //174
		width: 692upx;
		height: 184upx;
		background-color: #ffffff;
		box-shadow: 0upx 2upx 8upx 0upx rgba(0, 0, 0, 0.16);
		border-radius: 10upx;
		margin-left: 30upx;
	}
</style>
