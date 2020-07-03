<template>
	<view class="proposal">
		<textarea v-model="text" value="" placeholder="请输入建议/反馈" />
		<text class="len">{{text.length}}/300</text>
		<view class="button">提交</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				text: '',
			}
		},
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
	.proposal {
		height: 100vh;
		background-color: rgb(238, 238, 238);
	}
	textarea {
		padding: 20upx;
		width: 100%;
		height: 300upx;
		background-color: #FFFFFF;
	}
	
	.len {
		font-size: 30upx;
		position: fixed;
		right: 20upx;
		top: 350upx;
	}
	
	.button {
		margin: 30upx 0;
		width: 90%;
		margin-left: 50%;
		transform: translateX(-50%);
		background-color: rgb(242, 48, 48);
		text-align: center;
		border-radius: 35upx;
		color: #FFFFFF;
		padding: 10upx 0;
	}
</style>
