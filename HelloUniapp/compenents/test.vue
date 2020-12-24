<template>
	<view>
		{{ num }}
		{{ title }}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				num: 3
			}
		},
		props: ["title"],
		created() {
			console.log(this.num)
		}
	}
</script>

<style>
</style>
