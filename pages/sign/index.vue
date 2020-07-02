<template>
	<view class="sign">
		<view class="sign-list">
			<view class="sign-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="sign-list__info">
				<view class="sign-list__name">宪法</view>
				<view class="sign-list__date">2020-06-16</view>
				<view class="sign-list__date">14:35</view>
				<view class="sign-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>取消</view>
				</view>

			</view>
		</view>
		<view class="sign-list">
			<view class="sign-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="sign-list__info">
				<view class="sign-list__name">宪法</view>
				<view class="sign-list__date">2020-06-16</view>
				<view class="sign-list__date">14:35</view>
				<view class="sign-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>取消</view>
				</view>

			</view>
		</view>
		<view class="sign-list">
			<view class="sign-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="sign-list__info">
				<view class="sign-list__name">宪法</view>
				<view class="sign-list__date">2020-06-16</view>
				<view class="sign-list__date">14:35</view>
				<view class="sign-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>取消</view>
				</view>

			</view>
		</view>
		<view class="sign-list">
			<view class="sign-list__content">《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立…</view>
			<view class="sign-list__info">
				<view class="sign-list__name">宪法</view>
				<view class="sign-list__date">2020-06-16</view>
				<view class="sign-list__date">14:35</view>
				<view class="sign-list__status">
					<image src="../../static/fail.png" mode=""></image>
					<view>取消</view>
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
	.sign {
		display: flex;
		flex-direction: column;
	}

	.sign-list {
		margin: 0 21upx;
		padding-top: 33upx;
		padding-bottom: 15upx;
		border-bottom: 1upx solid rgba(0, 0, 0, .2);
	}


	.sign-list__content {
		font-size: 30upx;
		line-height: 51upx;
		margin-bottom: 30upx;
	}

	.sign-list__info {
		position: relative;
		display: flex;
		font-size: 23upx;
	}

	.sign-list__name {
		font-size: 23upx;
		color: #000000;
		opacity: 0.5;
		width: 87upx;
	}

	.sign-list__date {
		color: #000000;
		opacity: 0.5;
		font-size: 23upx;
		width: 187upx;
	}

	.sign-list__status {
		display: flex;
		align-items: center;
		width: 120upx;
		position: absolute;
		right: 0upx;
	}
	
	.sign-list__status view {
		color: #000000;
		opacity: 0.5;
		font-size: 21upx;
	}

	.sign-list__status image {
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
