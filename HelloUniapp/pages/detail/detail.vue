<template>
	<view>
		<!-- <view>
			<text>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text selectable>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text electable space="ensp">唱歌　　跳舞打篮球</text>
		</view>
		<view>
			<text electable space="emsp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text electable space="emsp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text electable space="nbsp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text electable space="emsp" style="font-size:30px;">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text>&amp;</text>
		</view> -->
		
		<!-- view class="box2" hover-class="box2-active">
			<view
				class="box"
				hover-class="box-active"
				:hover-start-time="2000"
				:hover-stay-time="2000"
				hover-stop-propagation
			>我是一个大盒子</view>
		</view> -->
		
		<!-- <button>按钮</button>
		<button size="mini">按钮</button>
		<button type="primary">按钮</button>
		<button type="warn" plain>按钮</button>
		<button type="primary" disabled>按钮</button>
		<button loading></button> -->
		
		<image src="../../static/logo.png"></image>
		<image src="../../static/logo.png" mode="aspectFit"></image>
		<image src="../../static/logo.png" mode="aspectFill"></image>
		
	</view>
</template>

<script>
	export default {
		onLoad(options) {
			console.log(options)
		}
	}
</script>

<style>
	.box {
		width: 100px;
		height: 100px;
		background-color: #00aa00;
	}
	.box-active {
		background-color: #7FFF00;
	}
	.box2 {
		background-color: #007AFF;
	}
	.box2-active {
		background-color: #00ffff;
	}
</style>
