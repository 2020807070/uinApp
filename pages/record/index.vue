<template>
	<view class="record">
		<view class="record-list">
			<view class="record-list-item">
				<view class="record-list-item__top">
					<view class="record-list-item__tit">宪法知识答题主题</view>
					<view class="record-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="record-list-item__btm">
					<view class="record-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="record-list-item__btn">查看成绩</view>
				</view>
			</view>
		</view>
		<view class="record-list">
			<view class="record-list-item">
				<view class="record-list-item__top">
					<view class="record-list-item__tit">宪法知识答题主题</view>
					<view class="record-list-item__date">2020/06/01-2020/06/30</view>
				</view>
				<view class="record-list-item__btm">
					<view class="record-list-item__content">《中华人民共和国宪法》是中华国的根本大法，规定拥有最高法律效力。中华人和国成立后，</view>
					<view class="record-list-item__btn">查看成绩</view>
				</view>
			</view>
		</view>
	</view>
</template>

<style>
	.record-list {
		background-color: #FFFFFF;
	}
	
	.record-list-item {
		width: 727upx;
		margin-left: 13upx;
		display: flex;
		flex-direction: column;
		border-bottom: 1upx solid rgba(0, 0, 0, .3);
		padding: 22upx 0;
	}
	
	.record-list-item__top {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	
	.record-list-item__btm {
		margin-top: 20upx;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	
	.record-list-item__content {
		font-size: 24upx;
		width: 500upx;
		color: rgba(0, 0, 0, .7);
	}
	.record-list-item__btn{
		width: 202upx;
		height: 62upx;
		background-color: #25a3cb;
		border-radius: 31upx;
		color: #fff;
		font-size: 34upx;
		text-align: center;
		line-height: 62upx;
	 }
	
	.disabled {
		background-color: #a0a0a0;
	}
	.record-list-item__tit {
		font-size: 34upx;
	}
	.record-list-item__date {
		font-size: 20upx;
	}
</style>