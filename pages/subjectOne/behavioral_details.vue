<template>
	<view>
		<rili></rili>
		
		<view class="mt20 bgff">
			<view class="box pt20 pm20 fz32 btm pd">
				<view class="box_b ">
					行为扣除
				</view>
				<view class="box_a tr z3">
					-150
				</view>
			</view>
			<view class="box pt20 pm20 fz28 btm pd">
				<view class="box_b z9 ">
					检查罚单
				</view>
				<view class="box_a tr red">
					-150
				</view>
			</view>
		</view>
	</view>
</template>
<script>
	import rili from "../../components/rili.vue"
	export default {
		data() {
			return {}
		},
		components: {
			rili
		},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.red{
		color: #ff4300 !important;
	}
</style>
