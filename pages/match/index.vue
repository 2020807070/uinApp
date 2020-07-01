<template>
	<view class="mathc-wrapper">
		<image class="banner" src="../../static/home/banner.png" mode=""></image>
		<view class="match-list">
			<view class="match-item">
				<image class="match-item__cover" src="../../static/online/01.png" mode=""></image>
				<view class="match-item__info">
					<view class="match-item__info_top">
						<view class="match-item__tit">宪法知识答题主题</view>
						<view class="match-item__date">2020/06/01-2020/06/30</view>
					</view>
					<view class="match-item__info_bottom">
						<view class="match-item__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立后，</view>
						<view class="match-item__btn">去答题</view>
					</view>
				</view>
			</view>
			<view class="match-item">
				<image class="match-item__cover" src="../../static/online/03.png" mode=""></image>
				<view class="match-item__info">
					<view class="match-item__info_top">
						<view class="match-item__tit">宪法知识答题主题</view>
						<view class="match-item__date">2020/06/01-2020/06/30</view>
					</view>
					<view class="match-item__info_bottom">
						<view class="match-item__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立后，</view>
						<view class="match-item__btn disabled">查看</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<style>
	.banner {
		width: 100%;
		height: 364upx;
	}
	
	.match-list {
		min-height: 1200upx;
		margin-bottom: 400upx;
	}
	
	.match-item {
		margin-top: 30upx;
		width: 100%;
		padding: 0;
		overflow: hidden;
		border-bottom: 2upx solid rgba(168, 168, 168, 0.5);
	}

	.match-item__cover {
		border-radius: 10upx;
		width: 716upx;
		height: 358upx;
		transform: translateX(-50%);
		margin-left: 50%;
	}

	.match-item__info {
		padding: 0 14upx;
	}

	.match-item__info_top {
		margin-bottom: 14upx;
		margin: 30upx 0;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.match-item__info_bottom {
		justify-content: space-between;
		display: flex;
		margin-bottom: 14upx;
	}

	.match-item__tit {
		font-size: 34upx;
		color: #000000;
	}

	.match-item__date {
		font-size: 20upx;
		color: #000000;
		opacity: 0.8;
	}

	.match-item__content {
		width: 510upx;
		font-size: 10upx;
		letter-spacing: 0upx;
		color: #000000;
		opacity: 0.7;
	}

	.match-item__btn {
		color: #fff;
		text-align: center;
		line-height: 62upx;
		width: 202upx;
		height: 62upx;
		background-color: #bf1111;
		border-radius: 32upx;
		font-size: 34upx;
	}
	.disabled {
		background-color: #a0a0a0;
	}
</style>
