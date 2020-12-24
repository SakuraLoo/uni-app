<template>
	<view>
		<view>《导航跳转的学习》</view>
		<navigator url="/pages/detail/detail?id=80">跳转至详情页</navigator>
		<navigator url="/pages/message/message" open-type="switchTab">跳转至信息页</navigator>
		<navigator url="/pages/detail/detail" open-type="redirect">跳转至详情页</navigator>
		
		<button @click="GoDetail">跳转至详情页</button>
		<button @click="GoMessage">跳转至信息页</button>
		<button @click="ReMessage">跳转至详情页并关闭当前页面</button>
	</view>
</template>

<script>
	export default {
		methods: {
			onUnload() {
				console.log("导航页面卸载了") // redirect的时候
			},
			GoDetail() {
				uni.navigateTo({
					url: "/pages/detail/detail"
				})
			},
			GoMessage() {
				uni.switchTab({
					url: "../message/message"
				})
			},
			ReMessage() {
				uni.redirectTo({
					url: "/pages/detail/detail"
				})
			}
		}
	}
</script>

<style>
</style>
