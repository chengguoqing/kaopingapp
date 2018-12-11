<template>
	<view>
		<view class="pd pt20 pm20 fz28 z3 bgff bbm">
			所属部门：软件事业部
		</view>
		<rili_gx></rili_gx>
		<view class="bgff btm pt20 fz28 z3 pm20 pd">
			选定日期：  2018年8月25日
		</view>
		
		<view class="mt100 dx_row pd ">
			<view class="dx_col_12 pr30">
				<navigator url="" class="dx_btn">设置为公休日</navigator>
			</view>
			<view class="dx_col_12 pl30">
				<navigator url="" class="dx_btn">设置为非公休日</navigator>
			</view>
		</view>
		
	</view>
</template>
<script>
	import rili_gx from "@/components/rili_gx.vue"
	export default {
		data() {
			return {}
		},
		components: {
			rili_gx
		},
		methods: {},
		mounted() {},
	}
</script>
<style scoped></style>
