<template>
	<view class="ranking">
		<view class="ranking-card">
			<view class="ranking-info">
				<image class="ranking-info__head" src="../../static/nav/match.png" mode=""></image>
				<view class="ranking-info__name" >甲乙丙丁</view>
				<!-- <view class="ranking-info__num">第二名</view> -->
				<view class="ranking-info__num">您未参与, 暂无排名</view>
				<view class="ranking-info__count">
					<view>获得积分</view>
					<view class="count">250</view>
				</view>
			</view>
		</view>
		<view class="ranking-list">
			<view class="ranking-item" v-for="(rankItem, ind) in ranklist">
				<view class="ranking-item__num">{{ind + 1}}</view>
				<image class="ranking-item__head" src="../../static/nav/online-a.png" mode=""></image>
				<view class="ranking-item__name">{{rankItem.name}}</view>
				<view class="ranking-item__count">{{rankItem.count}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				ranklist: [
					{
						count: 300,
						name: '逃之夭夭',
					},
					{
						count: 250,
						name: '防辐射',
					},
					{
						count: 240,
						name: '黄眼睛',
					},
					{
						count: 230,
						name: '大大发',
					},
					{
						count: 10,
						name: '的地方',
					},
					{
						count: 5,
						name: '大大',
					}
				]
			}
		}
	}
</script>
<style>
	.ranking-card {
		padding: 32upx 0;
		border-bottom: 14upx solid rgb(229, 229, 229);
	}

	.ranking-info__head {
		width: 104upx;
		height: 104upx;
		border-right: 50%;
		margin: 0 23upx 0 21upx;
		margin-top: 17upx;
	}
	
	.ranking-info__name {
		font-size: 36upx;
		margin-top: 17upx;
	}
	
	.ranking-info__num {
		position: absolute;
		top: 27upx;
		left: 50%;
		transform: translateX(-50%);
		font-size: 30upx;
		color: #be3737;
	}
	
	.ranking-info__count {
		text-align: center;
		position: absolute;
		right: 27upx;
		width: 138upx;
		color: #41afd2;
		font-size: 35upx;
		margin-top: 17upx;
	}
	.ranking-info__count .count {
		font-size: 48upx;
		margin-top: 6upx;
	}
	
	.ranking-info {
		height: 182upx;
		display: flex;
		align-items: center;
		position: relative;
		margin-left: 50%;
		transform: translateX(-50%);
		width: 664upx;
		background-color: #ffffff;
		box-shadow: 0upx 1upx 7upx 0upx 
			rgba(0, 0, 0, 0.16);
		border-radius: 10upx;
	}
	.ranking-item {
		position: relative;
		display: flex;
		height: 113upx;
		align-items: center;
		border-bottom: 1upx solid rgba(0, 0, 0, .2);
	}
	.ranking-item__head {
		width: 78upx;
		height: 78upx;
		margin-right: 23upx;
		border-right: 50%;
	}
	.ranking-item__name {
		font-size: 26upx;
	}
	.ranking-item__num {
		font-size: 34upx;
		font-weight: 600;
		padding: 0 35upx;
	}
	.ranking-item__count {
		position: absolute;
		right: 50upx;
		font-size: 48upx;
		color: #41afd2;
	}
</style>
