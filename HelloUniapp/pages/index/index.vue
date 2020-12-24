<template>
	<view class="content">
		<test v-if="flag" :title="title"></test>
		<button @click="checkTest">切换test组件</button>
	</view>
</template>

<script>
	import test from "../../compenents/test.vue"
	export default {
		data() {
			return {
				flag: true,
				title: "aaa"
			}
		},
		methods: {
			checkTest() {
				this.flag = !this.flag;
			}
		}
	}
</script>

<style>
</style>
