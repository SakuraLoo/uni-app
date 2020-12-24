<template>
	<view>
		<button @click="GetAjax">发送get请求</button>
		<button type="primary" @click="SetStoragy">存储数据</button>
		<button @click="GetStoragy">获取数据</button>
		<button type="primary" @click="RemoveStoragy">移除id</button>
		<view>这是列表页</view>
		<view class="box-item" v-for="item in list">
			{{ item }}
		</view>
		<!-- <button @click="Pulldown">点击刷新</button> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ["aaa","bbb","ccc","ddd","eee","aaa","bbb","ccc","ddd","eee"]
			}
		},
		onPullDownRefresh() {
			setTimeout(() => {
				this.list = ["a","b","c","d","e","a","b","c","d","e"];
				uni.stopPullDownRefresh();
			}, 2000)
		},
		onReachBottom() {
			console.log("页面触底了")
		},
		
		methods: {
			// Pulldown() {
			// 	uni.startPullDownRefresh();
			// }
			GetAjax() {
				uni.request({
					url: "http://mock.shtodream.cn/mock/5fa8fc178e13766542114da6/mimal/carts",
					success(res) {
						console.log(res)
					}
				})
			},
			SetStoragy() {
				// uni.setStorage({
				// 	key: "id",
				// 	data: 80,
				// 	success() {
				// 		console.log("存储成功")
				// 	}
				// })
				uni.setStorageSync("id",100);
			},
			GetStoragy() {
				// uni.getStorage({
				// 	key: "id",
				// 	success(res) {
				// 		console.log(res)
				// 	}
				// })
				const res = uni.getStorageSync("id");
				console.log(res)
			},
			RemoveStoragy() {
				uni.removeStorage({
					key: "id",
					success() {
						console.log("删除成功")
					}
				})
			}
		}
	}
</script>

<style>
	.box-item {
		height: 100px;
		line-height: 100px;
	}
</style>
