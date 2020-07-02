<template>
	<view class="search">
		<view class="search-list">
			<view class="search-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="search-list__info">
				<view class="search-list__name">宪法</view>
				<view class="search-list__date">2020-06-16</view>
				<view class="search-list__date">14:35</view>
				<view class="search-list__status success">
					<image src="../../static/success.png" mode=""></image>
					<view>已学会</view>
				</view>

			</view>
		</view>
		<view class="search-list">
			<view class="search-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="search-list__info">
				<view class="search-list__name">宪法</view>
				<view class="search-list__date">2020-06-16</view>
				<view class="search-list__date">14:35</view>
				<view class="search-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>未学习</view>
				</view>

			</view>
		</view>
		<view class="search-list">
			<view class="search-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="search-list__info">
				<view class="search-list__name">宪法</view>
				<view class="search-list__date">2020-06-16</view>
				<view class="search-list__date">14:35</view>
				<view class="search-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>未学习</view>
				</view>

			</view>
		</view>
		<view class="search-list">
			<view class="search-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="search-list__info">
				<view class="search-list__name">宪法</view>
				<view class="search-list__date">2020-06-16</view>
				<view class="search-list__date">14:35</view>
				<view class="search-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>未学习</view>
				</view>

			</view>
		</view>
		<view class="search-list">
			<view class="search-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="search-list__info">
				<view class="search-list__name">宪法</view>
				<view class="search-list__date">2020-06-16</view>
				<view class="search-list__date">14:35</view>
				<view class="search-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>未学习</view>
				</view>

			</view>
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
	.search {
		display: flex;
		flex-direction: column;
	}

	.search-list {
		margin: 0 21upx;
		padding-top: 33upx;
		padding-bottom: 15upx;
		border-bottom: 1upx solid rgba(0, 0, 0, .2);
	}


	.search-list__content {
		font-size: 30upx;
		line-height: 51upx;
		margin-bottom: 30upx;
	}

	.search-list__info {
		position: relative;
		display: flex;
		font-size: 23upx;
	}

	.search-list__name {
		font-size: 23upx;
		color: #000000;
		opacity: 0.5;
		width: 87upx;
	}

	.search-list__date {
		color: #000000;
		opacity: 0.5;
		font-size: 23upx;
		width: 187upx;
	}

	.search-list__status {
		display: flex;
		align-items: center;
		width: 120upx;
		position: absolute;
		right: 0upx;
	}
	
	.search-list__status view {
		color: #000000;
		opacity: 0.5;
		font-size: 21upx;
	}

	.search-list__status image {
		width: 23upx;
		height: 23upx;
		color: #000000;
		opacity: 0.5;
		margin-right: 8upx;
	}

	.success {
		color: #25a3cb;
	}
</style>
