<!-- 异常申诉 -->
<template>
	<view class="pm50">
		<rili :is_ddf="is_ddf" is_down="act"></rili>

		<view class="btm pd pt20  bgff">
			<view class=" pt10  ln">
				<view class="fz30 z3">
					上班打卡时间07：50 <text class="red">随机抽查超时未响应</text>
				</view>
				<view class=" z9 fz26">
					海南省海口市迎宾路棕榈公寓
				</view>
			</view>
		</view>




		<view class="bgff pt20  pt20">


			<view class="dx_row pd pt10  fz28 ">
				<view class="dx_col_6 df_df_dsrtxr">
					申诉类型：
				</view>
				<view class="ov pr20">
					<view class="f_b pr">
						<picker class="picker-item" mode="selector" :range="textList">
							<input type="text" value=" 打卡失败" disabled class="df_jh_ddfrxe br ac" />
							<icon class="dx icon-down doing_eert"></icon>
						</picker>
					</view>


				</view>
			</view>


			<view class="dx_row pd pt10  fz28 ">
				<view class="dx_col_6 df_df_dsrtxr">
					申诉理由：
				</view>
				<view class="ov pr20">
					<view class="f_b pr">
						<input type="text" value=" 网络异常" class="df_jh_ddfrxe br ac" />

					</view>


				</view>
			</view>






			<view class="dx_row pd pt10  fz28 ">
				<view class="dx_col_6 df_df_dsrtxr">
					申诉详情
				</view>
				<view class="ov ">
					<textarea value="" placeholder="请输入申诉详情" class="sd_kh_deert" />
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
							
							<view class="dd_dr_row mb20" @click="xztu">
								<image src="../../../static/img/add_icon.png" class="add_icon"></image>
							</view>
							
							
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
			return {
				is_ddf:true,
				textList: [
					'text1',
					'text2',
					'text3'
				],
			}
		},
		components: {
			rili
		},
		methods: {
			xztu() {
				uni.chooseImage({
					count: 6, //默认9
					sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
					sourceType: ['album'], //从相册选择
					success: function(res) {
						console.log(JSON.stringify(res.tempFilePaths));
					}
				});
			},
		},
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
