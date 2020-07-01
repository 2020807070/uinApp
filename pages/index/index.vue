<template>
	<view class="wrapper">
		<view class="main">
			<home v-if="tab === 'home'" />
			<match v-if="tab === 'match'" />
			<online v-if="tab === 'online'" />
			<mine v-if="tab === 'mine'" />
		</view>
		<view class="footer">
			<view class="footer-item" v-for="(navItem, ind) in tabList" :key="ind" @click="togglePages(navItem)">{{ navItem.name }}</view>
		</view>
	</view>
</template>

<script>
	import home from '@/pages/home/index.vue'
	import match from '@/pages/match/index.vue'
	import online from '@/pages/online/index.vue'
	import mine from '@/pages/mine/index.vue'

	export default {
		data() {
			return {
				tab: 'home',
				tabList: [{
						name: '首页',
						key: 'home',
					},
					{
						name: '答题竞赛',
						key: 'match',
					},
					{
						name: '在线学习',
						key: 'online',
					},
					{
						name: '个人中心',
						key: 'mine',
					},
				]
			};
		},
		components: {
			home,
			mine,
			match,
			online
		},
		methods: {
			togglePages(item) {
				this.tab = item.key;
			}
		}
	};
</script>

<style>
	.center {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.wrapper {
		width: 100%;
		height: 100vh;
		display: flex;
		flex-direction: column;
	}

	.main {
		flex: 1;
		overflow-y: scroll;
		/* background-color: rgb(245, 245, 245); */
	}

	.footer {
		border-top: solid 1upx #b5b5b5;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 114upx;
		background-color: fff;
	}

	.footer-item {
		flex: 1;
	}
</style>
