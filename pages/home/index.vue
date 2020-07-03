<template>
	<view class="home">
		<view class="nav-bar">
			<image class="logo" src="../../static/common/logo.png" mode=""></image>
			<view class="input">
				<image src="../../static/home/搜索.png" mode=""></image>
				<input type="text" placeholder="立即答题">
			</view>
			<view class="count">
				<view class="text">积分</view>
				<view class="num">250</view>
			</view>
		</view>
		<view class="home-title"></view>
		<view class="scroll-tab"></view>
		<view class="home-banner">
			<image src="../../static/home/banner.png" mode=""></image>
		</view>
		<view class="home-list">
			<view class="home-list-item">
				<view class="home-list-item__top">
					<view class="home-list-item__tit">宪法知识答题主题</view>
					<view class="home-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="home-list-item__btm">
					<view class="home-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="home-list-item__btn" @click="goAsk">去答题</view>
				</view>
			</view>
			<view class="home-list-item">
				<view class="home-list-item__top">
					<view class="home-list-item__tit">宪法知识答题主题</view>
					<view class="home-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="home-list-item__btm">
					<view class="home-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="home-list-item__btn" @click="goAsk">去答题</view>
				</view>
			</view>
			<view class="home-list-item">
				<view class="home-list-item__top">
					<view class="home-list-item__tit">宪法知识答题主题</view>
					<view class="home-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="home-list-item__btm">
					<view class="home-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="home-list-item__btn" @click="goAsk">去答题</view>
				</view>
			</view>
			<view class="home-list-item">
				<view class="home-list-item__top">
					<view class="home-list-item__tit">宪法知识答题主题</view>
					<view class="home-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="home-list-item__btm">
					<view class="home-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="home-list-item__btn disabled">查看</view>
				</view>
			</view>
		</view>
		<view class="sub-title">
			<view class="sub-title-main">
				<image style="width: 39upx;height: 36upx;padding: 0 18upx;" src="../../static/home/star.png" mode=""></image>
				<view class="sub-title__black">在线</view>
				<view class="sub-title__red">学法</view>
				<image style="width: 39upx;height: 36upx;" src="../../static/home/star.png" mode=""></image>
			</view>
			<image class="sub-title__more" src="../../static/home/more.png" mode=""></image>
		</view>
		<scroll-view class="scroll-wrap" scroll-x="true">
			<view @click="checkItem(item)" :class="['scroll-item', {'active': item === currItem}]" v-for="(item, ind) in scrollList">{{ item }}</view>
		</scroll-view>
		<view class="home-list">
			<view class="home-list__container" @click="goArticle">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/03.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list">
			<view class="home-list__container" @click="goArticle">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/03.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list">
			<view class="home-list__container" @click="goArticle">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/03.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-title">
			<view class="sub-title-main">
				<image style="width: 39upx;height: 36upx;padding: 0 18upx;" src="../../static/home/star.png" mode=""></image>
				<view class="sub-title__black">法律</view>
				<view class="sub-title__red">要闻</view>
				<image style="width: 39upx;height: 36upx;" src="../../static/home/star.png" mode=""></image>
			</view>
			<image class="sub-title__more" src="../../static/home/more.png" mode=""></image>
		</view>
		<view class="news-list">
			<view class="new-list__l" @click="goArticle">
				<view class="new-list__t">国家安全法律法规知识看这里</view>
				<view class="new-list__c">全国人大常委会通过新的国家安全法，将4月15日定为全民国家安全教育通…</view>
				<view class="new-list__i">
					<text style="margin-right: 14upx;">劳动法</text>
					<text>2020-06-16</text>
				</view>
			</view>
			<image class="new-list__r" src="../../static/online/05.png" mode=""></image>
		</view>
		<view class="news-list">
			<view class="new-list__l" @click="goArticle">
				<view class="new-list__t">国家安全法律法规知识看这里</view>
				<view class="new-list__c">全国人大常委会通过新的国家安全法，将4月15日定为全民国家安全教育通…</view>
				<view class="new-list__i">
					<text style="margin-right: 14upx;">劳动法</text>
					<text>2020-06-16</text>
				</view>
			</view>
			<image class="new-list__r" src="../../static/online/06.png" mode=""></image>
		</view>
		<view class="news-list">
			<view class="new-list__l" @click="goArticle">
				<view class="new-list__t">2020二套房的判断标准是什么</view>
				<view class="new-list__c">全国人大常委会通过新的国家安全法，将4月15日定为全民国家安全教育通…</view>
				<view class="new-list__i">
					<text style="margin-right: 14upx;">劳动法</text>
					<text>2020-06-16</text>
				</view>
			</view>
			<image class="new-list__r" src="../../static/online/05.png" mode=""></image>
		</view>
		<view class="news-list">
			<view class="new-list__l" @click="goArticle">
				<view class="new-list__t">国家安全法律法规知识看这里</view>
				<view class="new-list__c">全国人大常委会通过新的国家安全法，将4月15日定为全民国家安全教育通…</view>
				<view class="new-list__i">
					<text style="margin-right: 14upx;">劳动法</text>
					<text>2020-06-16</text>
				</view>
			</view>
			<image class="new-list__r" src="../../static/online/07.png" mode=""></image>
		</view>
		<view class="sub-title">
			<view class="sub-title-main">
				<image style="width: 39upx;height: 36upx;padding: 0 18upx;" src="../../static/home/star.png" mode=""></image>
				<view class="sub-title__black">法务</view>
				<view class="sub-title__red">知识库</view>
				<image style="width: 39upx;height: 36upx;" src="../../static/home/star.png" mode=""></image>
			</view>
			<image class="sub-title__more" src="../../static/home/more.png" mode=""></image>
		</view>
		<scroll-view class="scroll-wrap" scroll-x="true">
			<view @click="checkItem(item)" :class="['scroll-item', {'active': item === currItem}]" v-for="(item, ind) in scrollList">{{ item }}</view>
		</scroll-view>
		<view class="knowledge-list">
			<image class="knowledge-list__banner" src="../../static/online/06.png" mode=""></image>
			<view class="knowledge-list__info">
				<view class="knowledge-list__title">扫黑除恶法律法规知识</view>
				<view class="knowledge-list__date">2020-06-16</view>
			</view>
			<view class="knowledge-list__content">
				扫黑律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法…
			</view>
		</view>
		<view class="knowledge-list">
			<image class="knowledge-list__banner" src="../../static/online/04.png" mode=""></image>
			<view class="knowledge-list__info">
				<view class="knowledge-list__title">扫黑除恶法律法规知识</view>
				<view class="knowledge-list__date">2020-06-16</view>
			</view>
			<view class="knowledge-list__content">
				扫黑律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法律法规知识扫黑除恶法…
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				currItem: '劳动法',
				scrollList: ['劳动法', '婚姻法', '民事法', '刑事法', '刑事法2',]
			}
		},
		methods: {
			goArticle () {
				uni.navigateTo({
					url: `/pages/article/index`
				});
			},
			goAsk () {
				uni.navigateTo({
					url: `/pages/onlineAnswer/index`
				});
			},
			checkItem (item) {
				this.currItem = item;
			}
		}
	}
</script>
<style>
	.home {
		overflow-x: hidden;
		height: 100%;
		background-color: rgb(245, 245, 245);
		padding-bottom: 100upx;
	}

	.home-banner image {
		width: 100%;
		height: 394upx;
		background-color: #ffffff;
	}

	.home-list {
		background-color: #FFFFFF;
	}

	.home-list-item {
		width: 727upx;
		display: flex;
		flex-direction: column;
		border-bottom: 1upx solid rgba(0, 0, 0, .3);
		padding: 22upx 0;
	}

	.home-list-item__top {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.home-list-item__btm {
		margin-top: 20upx;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.home-list-item__content {
		font-size: 24upx;
		width: 500upx;
		color: rgba(0, 0, 0, .7);
	}

	.home-list-item__btn {
		width: 202upx;
		height: 62upx;
		background-color: #bf1111;
		border-radius: 31upx;
		color: #fff;
		font-size: 34upx;
		text-align: center;
		line-height: 62upx;
	}

	.disabled {
		background-color: #a0a0a0;
	}

	.home-list-item__tit {
		font-size: 34upx;
	}

	.home-list-item__date {
		font-size: 20upx;
	}

	.sub-title {
		position: relative;
		margin-top: 73upx;
		padding: 17upx 0;
		border-bottom: 1px solid rgba(0, 0, 0, .2);
		background-color: #FFFFFF;
	}

	.sub-title-main {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-left: 50%;
		transform: translateX(-50%);
		font-size: 42upx;
	}

	.sub-title__red {
		font-weight: bolder;
		color: rgb(191, 17, 17);
	}

	.sub-title__black {
		font-weight: bolder;
		color: #000000;
	}

	.sub-title__more {
		position: absolute;
		top: 50%;
		transform: translateY(-50%);
		width: 15upx;
		height: 28upx;
		right: 17upx;
	}

	.home-list-item {
		padding: 28upx 15upx;
	}

	.home-list__title {
		font-size: 34upx;
		margin-bottom: 37upx;
		color: #000000;
	}

	.home-list__info {
		display: flex;
		margin-left: 20upx;
		padding-bottom: 20upx;
		border-bottom: 1upx solid rgb(0, 0, 0, .2);
	}

	.home-list__name {
		font-size: 23upx;
		color: #959595;
		margin-right: 103upx;
	}

	.home-list__commit {
		font-size: 23upx;
		color: #959595;
		margin-right: 75upx;
	}

	.home-list__date {
		font-size: 23upx;
		color: #959595;
		margin-right: 330upx;
	}

	.home-list__player {
		display: flex;
		align-items: center;
	}

	.home-list__player image {
		width: 26upx;
		height: 25upx;
		margin-right: 2upx;
	}

	.home-list__player view {
		font-size: 24upx;
		color: #dd1d11;
	}

	.home-list__container {
		display: flex;
		margin-left: 20upx;
		padding-top: 20upx;
	}

	.home-list__content {
		width: 484upx;
		line-height: 49upx;
		height: 122upx;
		font-size: 34upx;
		margin-right: 47upx;
		margin-bottom: 30upx;
	}

	.home-list__cover {
		width: 188upx;
		height: 122upx;
		border-radius: 6upx;
	}

	.news-list {
		padding: 32upx 0;
		background-color: #FFFFFF;
		display: flex;
		padding-left: 21upx;
		border-bottom: 1upx solid rgba(0, 0, 0, .3);
	}

	.new-list__l {
		width: 420upx;
	}

	.new-list__r {
		margin-left: 25upx;
		width: 271upx;
		height: 183upx;
		border-radius: 6upx;
	}

	.new-list__t {
		font-weight: 600;
		font-size: 30upx;
	}

	.new-list__c {
		font-size: 24upx;
		color: #313131;
		opacity: 0.7;
		margin: 22upx 0 30upx 0;
	}

	.new-list__i {
		font-size: 22upx;
		color: #959595;
		opacity: 0.8;
	}

	.knowledge-list {
		background-color: #FFFFFF;
		padding: 0 20upx;
		padding-top: 18upx;
		border-bottom: 1upx solid rgba(0, 0, 0, .3);
	}

	.knowledge-list__banner {
		width: 715upx;
		height: 385upx;
		border-radius: 10upx;
	}

	.knowledge-list__info {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 22upx 0 16upx 0;
	}

	.knowledge-list__title {
		font-size: 24upx;
		font-weight: bold;
	}

	.knowledge-list__date {
		font-size: 23upx;
		color: #959595;
		opacity: 0.8;
	}

	.knowledge-list__content {
		font-size: 21upx;
		color: #000000;
		opacity: 0.7;
		margin-bottom: 21upx;
	}

	.nav-bar {
		display: flex;
		align-items: center;
		background-color: #25a3cb;
		padding: 10upx 0;
	}

	.logo {
		width: 122upx;
		height: 36upx;
		padding: 0 12upx;
	}

	.input {
		display: flex;
		width: 440upx;
		height: 50upx;
		background-color: rgb(146, 209, 209);
		border-radius: 25upx;
		align-items: center;
	}
	
	.input image {
		margin: 0 12upx;
		width: 25upx;
		height: 25upx;
	}
	
	.input input {
		width: 80%;
		font-size: 20upx;
		color: rgb(94, 135, 148);
	}

	.count {
		color: #FFFFFF;
		display: flex;
		align-items: center;
	}

	.count .text {
		font-size: 28upx;
		margin-right: 6upx;
		margin-left: 19upx;
	}

	.count .num {
		font-size: 45upx;
	}
	
	.scroll-wrap {
		width: 100%;
		white-space: nowrap;
		padding: 20upx 0;
		background-color: #FFFFFF;
	}
	.scroll-item {
		font-size: 27upx;
		display: inline-block;
		border-right: 23upx;
		padding: 10upx 32upx;
		background-color: red;
		border-radius: 30upx;
		color: #FFFFFF;
		background-color: #b5b5b5;
		margin: 0 10upx;
	}
	
	.active {
		font-size: 32upx;
		background-color: #bf1111;
		padding: 12upx 39upx;
		border-radius: 35upx;
	}
</style>
