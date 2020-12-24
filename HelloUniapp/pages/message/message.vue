<template>
	<view>
		<button @click="chooseImg">上传图片</button>
		<image v-for="item in imgArr" :src="item" @click="previewImg(item)"></image>
		
		<!-- #ifdef H5 -->
		<view>只在h5中被看见</view>
		<!-- #endif -->
		
		<!-- #ifdef MP-WEIXIN -->
		<view>只在微信小程序中被看见</view>
		<!-- #endif -->
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgArr: []
			}
		},
		methods: {
			chooseImg() {
				uni.chooseImage({
					count: 5,
					success:res => {
						this.imgArr = res.tempFilePaths;
						console.log(res)
					}
				})
			},
			previewImg(current) {
				console.log(current)
				uni.previewImage({
					current,
					urls: this.imgArr,
					loop: true,
					indicator: "number"
				})
			}
		},
		onLoad() {
			// #ifdef H5
			console.log("只在h5中打印")
			// #endif
			
			// #ifdef MP-WEIXIN
			console.log("只在微信小程序中打印")
			// #endif
		}
	}
</script>

<style>
</style>
