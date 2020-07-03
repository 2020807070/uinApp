<template>
	<view class="center">
		<view class="center-top">
			<view class="center-tips">积分说明</view>
			<view class="center-main">
				<text>积分</text>
				<text class="center-count">10</text>
			</view>
		</view>
		<view class="center-list">
			<view class="center-list__item" v-for="(listItem, ind) in list" :key="ind">
				<view class="center-list__date">
					<view class="time">18:36</view>
					<view>2020-06-17</view>
				</view>
				<view class="center-list__source">{{listItem.source}}</view>
				<view class="center-list__count">
					<view class="num">+5</view>
					<view>总分：10</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						source: '阅读文章'
					},
					{
						source: '知识竞赛'
					}, {
						source: '阅读文章'
					},
					{
						source: '知识竞赛'
					}
				]
			}
		}
	}
</script>
<style>
	.center-top {
		display: flex;
		justify-content: center;
		align-items: center;
		position: relative;
		width: 100%;
		height: 289upx;
		background-color: #25a3cb;
	}

	.center-tips {
		position: absolute;
		top: 10upx;
		right: 10upx;
		font-size: 22upx;
		color: #eeeeee;
		opacity: 0.8;
	}

	.center-main {
		color: #fff;
		font-size: 50upx;
	}

	.center-count {
		font-size: 42upx;
		margin-left: 20upx;
		font-weight: 600;
	}

	.center-list__item {
		position: relative;
		display: flex;
		align-items: center;
		padding: 20upx 0;
		border-bottom: 1upx solid rgba(0, 0, 0, .3);
	}
	
	.center-list__date {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		padding-right: 15upx;
		width: 157upx;
		height: 93upx;
		border-right: 1upx solid rgba(0, 0, 0, .3);
		font-size: 25upx;
		color: #000000;
		opacity: 0.8;
	}
	
	.center-list__date .time {
		font-size: 36upx;
	}
	
	.center-list__source {
		margin-left: 40upx;
	}
	.center-list__count {
		height: 93upx;
		font-size: 26upx;
		position: absolute;
		right: 33upx;
		text-align: right;
		font-size: 26upx;
		color: #000000;
		opacity: 0.7;
	}
	.center-list__count .num {
		font-size: 47upx;
		color: #bf1111;
	}
</style>
