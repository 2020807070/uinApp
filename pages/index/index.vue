<template>
	<view class="wrapper">
		1231231
<!-- 		<view class="main">
			<home v-if="tab === 'home'" />
			<match v-if="tab === 'match'" />
			<online v-if="tab === 'online'" />
			<mine v-if="tab === 'mine'" />
		</view>
		<view class="footer" @click="aaa">
			<view class="footer-item" v-for="(navItem, ind) in tabList" :key="ind" @click="togglePages(navItem)">
				<image class="footer-img"  v-if="navItem.src" :src="tab === navItem.key ? navItem.srcA : navItem.src" mode=""></image>
				<view v-else>
					<image class="footer-icon" v-if="navItem.icon" :src="tab === navItem.key ? navItem.iconA : navItem.icon" mode=""></image>
					<view :class="['footer-text', {'active': tab === navItem.key } ]">{{ navItem.name }}</view>
				</view>
			</view>
		</view> -->
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
						icon: '../../static/nav/home.png',
						iconA: '../../static/nav/home-a.png',
					},
					{
						src: '../../static/nav/match.png',
						srcA: '../../static/nav/match-a.png',
						name: '答题竞赛',
						key: 'match',
					},
					{
						src: '../../static/nav/online.png',
						srcA: '../../static/nav/online-a.png',
						name: '在线学习',
						key: 'online',
					},
					{
						name: '个人中心',
						key: 'mine',
						icon: '../../static/nav/me.png',
						iconA: '../../static/nav/me-a.png',
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
			aaa (e) {
				e.preventDefault();
			},
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
		overflow: hidden;
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
		text-align: center;
	}
	
	.footer-img {
		width: 90upx;
		height: 90upx;
	}
	.footer-text {
		font-size: 24upx;
	}
	.footer-icon {
		width: 39upx;
		height: 40upx;
	}
	
	.active {
		color: rgb(37, 163, 203);
	}
</style>
