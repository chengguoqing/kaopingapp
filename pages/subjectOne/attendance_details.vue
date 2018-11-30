<template>
	<view>
		<rili></rili>
		
		<view class="mt20 bgff">
			<view class="box pt20 pm20 fz30 btm pd z3">
				<view class="box_b ">
					考勤扣除
				</view>
				<view class="box_a tr ">
					-150
				</view>
			</view>
			<view class="box pt20 pm20 fz30 btm pd z9">
				<view class="box_b ">
					迟到
				</view>
				<view class="box_a tr red">
					-150
				</view>
			</view>
			<view class="box pt20 pm20 fz30 btm pd z9">
				<view class="box_b ">
					早退
				</view>
				<view class="box_a tr red">
					-150
				</view>
			</view>
			<view class="box pt20 pm20 fz30 btm pd z9">
				<view class="box_b ">
					旷工
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
<style scoped></style>
