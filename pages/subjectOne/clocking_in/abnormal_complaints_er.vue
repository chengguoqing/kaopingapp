<!-- 异常申诉 -->
<template>
	<view class="pm50">
		<rili :is_ddf="is_ddf"></rili>
		
		<view class="btm pd pt20  bgff">
			<view class=" pt10 pm10 ln" >
				<view class="fz30 z3">
					上班打卡时间07：50 <text class="red">随机抽查超时未响应</text>
				</view>
				<view class=" z9 fz26">
					海南省海口市迎宾路棕榈公寓
				</view>
			</view>
		</view>
		
		
		
		
			<view class="bgff mt20  pt20">
		
		
					
					
					<view class="dx_row pd pt10  fz28 ">
									<view class="dx_col_6 df_df_dsrtxr">
									申诉类型：
									</view>
									<view class="ov pr20 df_df_dsrtxr z6">
					
										打卡失败
									</view>
								</view>
								
								
								<view class="dx_row pd pt10  fz28 ">
												<view class="dx_col_6 df_df_dsrtxr">
												申诉理由：
												</view>
												<view class="ov pr20 df_df_dsrtxr z6">
								
													网络异常
												</view>
											</view>
											
											
											
					<view class="dx_row pd pt10  fz28 ">
									<view class="dx_col_6 df_df_dsrtxr">
									申诉详情：
									</view>
									<view class="ov pr20 df_df_dsrtxr z6">
					
										手机的数据网络连接不了
									</view>
								</view>
					
								
								
								
					
					
		
		
		
					<view class="dx_row pd pt10  fz28 ">
						<view class="dx_col_6 df_df_dsrtxr">
							上传附件:
						</view>
						<view class="ov pr20 df_df_dsrtxr z6">
		
							<view class="dd_dr_row mb10">
								<image src="../../../static/img/bg_sdf.jpg" class="dmh_ddert cz"></image>
								<text class="ml10">附件1</text>
							</view>
							<view class="dd_dr_row mb10">
								<image src="../../../static/img/bg_sdf.jpg" class="dmh_ddert cz"></image>
								<text class="ml10">附件2</text>
							</view>
							
						</view>
					</view>
		
		
		
					
							<view class="dx_row pd pt10  fz28 ">
								<view class="dx_col_6 df_df_dsrtxr">
									申诉反馈：
								</view>
								<view class="ov ">
									<textarea value="" placeholder="请输入申诉反馈" class="sd_kh_deert" />
									</view>
							</view>
					
					
				</view>
				
				
				
				
				
		<view class="mt60 pd dx_row">
			<view class="dx_col_12 pr30">
				<navigator url="" class="dx_btn">同意</navigator>
			</view>
			<view class="dx_col_12 pl30">
				<navigator url="" class="dx_btn">退回</navigator>
			</view>
		</view>
		
	</view>
</template>
<script>
	import rili from "@/components/rili.vue"

	export default {
		data() {
			return {
				is_ddf:true
			}
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
	.dmh_ddert{
		width: 42upx;
		height: 39upx;
	}
	.add_icon{
		width: 67upx;
		height: 67upx;
	}
</style>
