<template>
	<view class="pages">
		<view v-show="isSort" class="sort" @click="sortHide">
			<view class="sort-title">题目表</view>
			<view class="sort-list">
				<view v-for="item in 24" :class="[{'list-active': item > 9}]">{{ item }}</view>
			</view>
			<image class="sort-icon" src="../../static/fail.png" mode=""></image>
		</view>
		<view class="card">
			<view class="question">
				<view class="question-tit">
					<text class="question-type">单选</text>
					社区矫正机构的设置和撤销，由___提出意见，按照规定的权限和程序审批。
				</view>
				<view class="question-answer" @click="check(ind)" v-for="(answerItem, ind) in answerList">
					<view :class="['radio', {'active': currInd === ind}]"></view>
					{{ answerItem }}
				</view>
			</view>
			<view class="result">
				<view class="result-title">标准答案为：D</view>
				<view class="result-mian">
					<view class="result-mian__tit">答案分析</view>
					<view class="result-mian__content">
						《中华人民共和国宪法》是中华人民共和国的根本大法，规定拥有最高法律效力。中华人民共和国成立后，曾于1954年9月20日、1975年1月17日、1978年3月5日和1982年12月4日通过四个宪法，现行宪法为1982年宪法。
					</view>
				</view>
			</view>
			<view class="card-bottom">
				<view class="sign">
					<image src="../../static/sign-1.png" mode=""></image>
					<view>标记</view>
				</view>
				<view class="progress" @click="sortShow">
					<image src="../../static/answer.png" mode=""></image>
					<view>1/20</view>
				</view>
				<view class="buttons">
					<view>上一题</view>
					<view>下一题</view>
				</view>
			</view>
		</view>
		<view class="btns">
			<view class="y">学会了</view>
			<view class="n">未学习</view>
		</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				isSort: false,
				currInd: 0,
				answerList: [
					'A、  乡、镇级人民政府司法行政部门',
					'B、  县级以上地方人民政府司法行政部门',
					'C、  地市级人民政府司法行政部门',
					'D、  省级人民政府司法行政部门'
				]
			}
		},
		methods: {
			sortShow () {
				this.isSort = true;
			},
			sortHide () {
				this.isSort = false;
			},
			check (ind) {
				this.currInd = ind;
			}
		}
	}
</script>
<style>
	.card {
		margin-left: 50%;
		transform: translateX(-50%);
		margin-top: 50upx;
		width: 710upx;
		min-height: 844upx;
		background-color: #ffffff;
		box-shadow: 0upx 0upx 6upx 0upx rgba(0, 0, 0, 0.19);
		border-radius: 10upx;
	}

	.result {
		margin-top: 70upx;
		width: 689upx;
		min-height: 216upx;
		border-radius: 10upx;
		border: 1upx solid #e76740;
		margin-left: 50%;
		transform: translateX(-50%);
	}

	.result-title {
		height: 57upx;
		line-height: 57upx;
		background-color: #e76740;
		color: #FFFFFF;
		font-size: 30upx;
		padding-left: 17upx;
	}

	.result-mian {
		margin: 0 13upx;
	}

	.result-mian__tit {
		color: #e76740;
		font-size: 24upx;
		margin-top: 21upx;
		margin-bottom: 15upx;
	}

	.result-mian__content {
		font-size: 24upx;
		margin-bottom: 32upx;
	}
	
	.question-answer {
		font-size: 22upx;
		margin: 13upx 0;
		display: flex;
		align-items: center;
		margin-left: 35upx;
	}
	
	.radio {
		width: 16upx;
		height: 16upx;
		border: solid 1upx #b5b5b5;
		border-radius: 50%;
		margin-right: 20upx;
	}
	
	.active {
		background-color: #41afd2;
	}
	
	.question {
	}
	.question-tit {
		width: 672upx;
		margin-left: 19upx;
		font-size: 30upx;
		padding: 50upx 0;
	}
	.question-type {
		font-size: 26upx;
		margin: 0 15upx;
		color: #a90000;
	}
	.card-bottom {
		display: flex;
		margin-top: 63upx;
	}
	
	
	.sign {
		display: flex;
		opacity: 0.6;
		align-items: center;
	}
	
	.sign view {
		font-size: 26upx;
	}
	
	.sign image {
		width: 25upx;
		height: 24upx;
	}
	.buttons {
		display: flex;
	}
	
	.buttons view {
		width: 186upx;
		height: 54upx;
		background-color: #37a7cb;
		border-radius: 10upx;
		font-size: 24upx;
		color: #fff;
		text-align: center;
		line-height: 54upx;
		margin-left: 21upx;
	}
	
	.progress {
		box-shadow: 0upx 0upx 6upx 0upx 
			rgba(0, 0, 0, 0.19);
		border-radius: 10upx;
		display: flex;
		opacity: 0.6;
		align-items: center;
		padding: 10upx 15upx;
		margin-left: 29upx;
		margin-right: 24upx;
	}
	
	.progress image {
		width: 32upx;
		height: 33upx;
	}
	
	.progress view {
		font-size: 24upx;
	}
	
	.btns {
		margin-left: 265upx;
		margin-top: 121upx;
		display: flex;
		flex-direction: column;
	}
	
	.btns view {
		width: 230upx;
		height: 68upx;
		background-color: #aaaaaa;
		border-radius: 10upx;
		font-size: 29upx;
		color: #ffffff;
		text-align: center;
		line-height: 68upx;
	}
	.btns .y {
		background-color: #be3737;
		margin-bottom: 33upx;
	}
	
	.sort {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0 ,0 ,0 , .6);
		z-index: 9999;
	}
	
	.sort-title {
		margin-left: 50%;
		transform: translateX(-50%);
		margin-top: 143upx;
		font-size: 36upx;
		color: #FFFFFF;
		text-align: center;
	}
	
	.sort-list {
		flex-wrap: wrap;
		display: flex;
		margin-left: 50%;
		transform: translateX(-50%);
		margin-top: 54upx;
		width: 663upx;
		height: 320upx;
		background-color: #ffffff;
		border-radius: 10upx;
	}
	.sort-list view {
		margin-top: 28upx;
		margin-left: 28upx;
		width: 7.5%;
		font-size: 30upx;
		color: #000000;
	}
	
	
	.sort-icon {
		margin-left: 50%;
		transform: translateX(-50%);
		margin-top: 50upx;
		width: 49upx;
		height: 49upx;
	}
	.sort-list .list-active {
		color: #a90000;
	}
	
</style>
