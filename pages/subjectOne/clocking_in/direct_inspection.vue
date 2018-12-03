<template>
	<view class="pm50">
		<rili></rili>

		<view class="btm pd pt20 pm20 bgff">
			<view class="mt20 pt10 pm10 ln" v-for="sd in 3">
				<view class="fz30 z3">
					上班打卡时间07：50 <text class="ls_er">验证通过</text>
				</view>
				<view class=" z9 fz26">
					海南省海口市迎宾路棕榈公寓
				</view>
			</view>
		</view>

		<view class="bgff mt20 pt20">


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_6 df_df_dsrtxr">
					直检结果：
				</view>
				<view class="ov pr20">
					<view class="f_b pr">
						<input type="text" value=" 早退"  disabled class="df_jh_ddfrxe br ac" />
						<icon class="dx icon-down doing_eert"></icon>
					</view>
					

				</view>
			</view>
			
			<view class="dx_row pd pt10 pm10 fz28 pm20">
				<view class="dx_col_6 df_df_dsrtxr">
					违约金：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					20元
				</view>
			</view>



			<view class="dx_row pd pt10 pm10 fz28 pm20">
				<view class="dx_col_6 df_df_dsrtxr">
					连带违约金：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					20元

				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 pm20">
				<view class="dx_col_6 df_df_dsrtxr">
					连带责任人：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					刘峰
				</view>
			</view>



			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_6 df_df_dsrtxr">
					直检原因：
				</view>
				<view class="ov ">
					<textarea value="" placeholder="请输入审查理由" class="sd_kh_deert" />
					</view>
			</view>
			
			
		</view>
		
		
		<view class="mt60 pd">
			<navigator url="" class="dx_btn">确定</navigator>
		</view>
	</view>
</template>
<script>
	import rili from "@/components/rili.vue"

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
	.doing_eert{
		position: absolute;
		right: 10upx;
		top: 0upx;
		z-index: 100;
	}
</style>
