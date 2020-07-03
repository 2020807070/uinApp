<template>
	<view class="article">
		<view class="article-wrap">
			<view class="article-title">开展"全民国家安全教育"法制宣传活动</view>
			<view class="article-date">2020-04-13</view>
			<view class="article-content">大叔大婶大大厦三点了看得见阿卡丽了框架垃圾筐。所</view>
			<view class="article-content">大萨达萨达金坷垃四大皆空拉三等奖打了卡打死了看得见阿斯利康聚隆科技离开的骄傲。</view>
			<view class="article-content">
				大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了
				大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大
				萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上
				课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都
				来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达
				撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了
				大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大
				萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家
				都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了
				大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒
				记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒
				上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录
				打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课
				了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看
				见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家
				都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大
				萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课
				了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家
				撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了
				大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看
				见了大萨达撒上课了大家都来撒记录打开
				看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都
				来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了大萨达撒上课了大家都来撒记录打开看见了</view>
		</view>
		<cover-view class="share">
			<image src=../../static/share.png mode=""></image>
		</cover-view>
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

.article {
	background-color: rgb(238, 238, 238);
	overflow: hidden;
}
.article-wrap {
	margin-top: 30upx;
	background-color: #FFFFFF;
	margin-bottom: 100upx;
}

.article-title {
	font-weight: 600;
	font-size: 45upx;
	padding: 10upx 15upx;
}

.article-date {
	margin-left: 15upx;
	font-size: 25upx;
	padding: 10upx 0;
	color: rgba(0, 0, 0, .6);
}

.article-content {
	margin-top: 30upx;
	text-indent: 2em;
	margin-left: 15upx;
	font-size: 35upx;
	padding: 10upx 0;
	color: rgba(0, 0, 0, .8);
}

.share {
	border-top: 3upx solid rgba(0, 0, 0, .3);
	position: fixed;
	bottom: 0;
	width: 100%;
	background-color: #FFFFFF;
	height: 100upx;
}

.share image {
	position: absolute;
	width: 50upx;
	height: 49upx;
	left: 50%;
	top: 50%;
	transform: translate3d(-50%, -50%, 0);
}
</style>
