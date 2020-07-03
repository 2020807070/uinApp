<template>
	<view class="online">
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
		<scroll-view class="scroll-tab" scroll-x="true">
			<view @click="checkItem(item)" :class="['tab-item', {'active': item === currItem}]" v-for="(item, ind) in scrollList">{{ item }}</view>
		</scroll-view>
		<view class="home-title"></view>
		<view class="home-banner">
			<image src="../../static/online/01.png" mode=""></image>
		</view>
		<view class="sub-tittle">
			习近平：充分认识颁布实施民法典重大意义 依法更好保障人民权益 
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020二套房的判断标准是什么</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020二套房的判断标准是什么</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">维护国家安全，应当遵守宪法和坚持会主义法治原则，尊重和保障人权，依…</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-banner">
			<image src="../../static/online/02.png" mode=""></image>
		</view>
		<view class="sub-nav">
			<view>劳动法</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/03.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/04.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-nav">
			<view>每日播报</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="home-live">
			<image src="../../static/online/05.png" mode=""></image>
			<view class="home-live__timer">06:26</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
			</view>
		</view>
		<view class="sub-nav">
			<view>新婚姻法</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="suv-nav__title">今日劳动法热门</view>
		<view class="home-live">
			<image src="../../static/online/06.png" mode=""></image>
			<view class="home-live__timer">06:26</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-nav">
			<view>刑事法</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="home-live">
			<image src="../../static/online/01.png" mode=""></image>
			<view class="home-live__timer">06:26</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/04.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/04.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/04.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-nav">
			<view>每日学法</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="home-live">
			<image src="../../static/online/05.png" mode=""></image>
			<view class="home-live__timer">06:26</view>
		</view>
		<view class="sub-nav">
			<view>未成年人保护法</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<view class="suv-nav__title">2020新未成年人保护法</view>
		<view class="home-live">
			<image src="../../static/online/07.png" mode=""></image>
			<view class="home-live__timer">06:26</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__container">
				<view class="home-list__content">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
				<image class="home-list__cover" src="../../static/online/03.png" mode=""></image>
			</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="sub-nav">
			<view>新法推荐</view>
			<image  class="sub-nav__more" src="../../static/home/more.png"></image>
		</view>
		<scroll-view class="scroll-wrap" scroll-x="true">
			<view class="scroll-item">
				<image class="scroll-item__cover" src="../../static/online/01.png" mode=""></image>
				<view class="scroll-item__info">
					<view class="title">颁布新民法典的重大意义</view>
					<view class="name">民事法</view>
				</view>
			</view>
			<view class="scroll-item">
				<image class="scroll-item__cover" src="../../static/online/06.png" mode=""></image>
				<view class="scroll-item__info">
					<view class="title">颁布新民法典的重大意义</view>
					<view class="name">民事法</view>
				</view>
			</view>
		</scroll-view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
		<view class="home-list" @click="goArticle">
			<view class="home-list__title">2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定2020年婚姻法新规定</view>
			<view class="home-list__info">
				<view class="home-list__name">民事法</view>
				<view class="home-list__commit">37评</view>
				<view class="home-list__date">2020-06-16</view>
				<view class="home-list__player">
					<image src="../../static/online/audio.png" mode=""></image>
					<view>播放</view>
				</view>
			</view>
		</view>
	</view>
</template>
<script>
	export default {
		data () {
			return {
				currItem: '全部',
				scrollList: ['全部', '劳动法', '婚姻法', '民事法', '刑事法', '刑事法2', '未成年人保护法',]
			}
		},
		methods: {
			goArticle () {
				uni.navigateTo({
					url: `/pages/article/index`
				});
			},
			checkItem (item) {
				this.currItem = item;
			}
		}
	}
</script>
<style>
	.online {
		background-color: rgb(245, 245, 245);
	}
	.home-banner image{
		width: 100%;
		height: 446upx;
		background-color: #ffffff;
	}
	.sub-tittle {
		padding: 10upx 13upx;;
		font-weight: bolder;
		font-size: 40upx;
	}
	.home-list {
		margin: 0 15upx;
		padding: 28upx 0;
		border-bottom: 1upx solid rgba(0,0,0,.3);
	}
	.home-list__title {
		font-size: 34upx;
		margin-bottom: 37upx;
		color: #000000;
	}
	.home-list__info {
		display: flex;
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
		margin-right: 230upx;
	}
	.home-list__player {
		display: flex;
		align-items: center;
	}
	.home-list__player image{
		width: 26upx;
		height: 25upx;
		margin-right: 2upx;
	}
	.home-list__player view{
		font-size: 24upx;
		color: #dd1d11;
	}
	
	.home-list__container {
		display: flex;
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
	.sub-banner image{
		width: 716upx;
		height: 267upx;
		margin: 14upx;
	}
	
	.sub-nav {
		margin-top: 49upx;
		margin: 32upx;
		position: relative;
		border-left: 10upx solid #dd1d11;
		margin-left: 15upx;
		height: 38upx;
		line-height: 38upx;
		text-indent: 19upx;
	}
	
	.sub-nav__more {
		position: absolute;
		top: 0;
		right: 19upx;
		width: 17upx;
		height: 29upx;
	}
	
	.suv-nav__title {
		margin-left: 19upx;
		margin-bottom: 12upx;
		font-size: 36upx;
	}
	.home-live {
		position: relative;
		height: 376upx;
	}
	.home-live image{
		width: 716upx;
		height: 376upx;
		border-radius: 10upx;
		margin-left: 17upx;
	}
	
	.home-live__timer {
		position: absolute;
		left: 31upx;
		font-size: 26upx;
		bottom: 14upx;
		width: 119upx;
		height: 40upx;
		text-align: center;
		line-height: 40upx;
		color: #fff;
		background-color: #000000;
		border-radius: 10upx;
		opacity: 0.7;
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
		height: 400upx;
	}
	.scroll-item {
		display: flex;
		flex-direction: column;
		margin: 0 11upx;
		display: inline-block;
		width: 438upx;
		height: 380upx;
		background-color: #ffffff;
		box-shadow: 0upx 1upx 7upx 0upx 
			rgba(0, 0, 0, 0.16);
		border-radius: 10upx;
	}
	
	.scroll-item__cover {
		height: 271upx;
		width: 100%;
		border-top-right-radius: 10upx;
		border-top-left-radius: 10upx;
	}
	
	.scroll-item__info {
		width: 109upx;
		margin-left: 12upx;
		padding-bottom: 10upx;
		
	}
	.scroll-item__info .title {
		font-size: 34upx;
	}
	.scroll-item__info .name{
		margin-top: 10upx;
		color: #959595;
		font-size: 23upx;
	 }
	 
	 .scroll-tab {
		padding-top: 15upx;
	 	width: 100%;
	 	white-space: nowrap;
	 	height: 67upx;
	 	background-color: #FFFFFF;
	 }
	 
	 .tab-item {
		text-align: center;
		width: 109upx;
		height: 48upx;
		font-size: 28upx;
	 	display: inline-block;
	 	color: #898989;
	 	margin: 0 10upx;
	 }
	 
	 
	 .active {
		color: #bf1111;
		border-bottom: 5upx solid #bf1111;
	 }
</style>